---
title: "Handwritten Notes"
date: 2024-04-01T05:56:14+01:00
description: I've tried to figure and configure xournalpp with a graphic tablet, it appears to be more effective than taking notes on paper.
tags:
  - workflow
  - notes
  - software
  - technology
---

## preamble

The last few weeks I've had to do a lot of learning for mathematics, that means just solving and trying to understand tasks around six hours day (afterwards the brain stops working). But that has brought me to an issue of the notes I've taken by hand. So time has come to rethink another part of my workflow.


## Starting point: notes on paper
{{< figure src="../../handwritten/notes.jpg" title="Figure 1: Handwritten notes" >}} 

I enjoy taking notes on paper, it appears reasonable and is the most intuitive. 

I use nice dotted 90g paper, an ink-pen, variety of mechanical pencils, fine ink-pens, etc.
It's fun using it, but having four pens, eraser and specific paper in a workflow, how reasonable can it be?

Mathematics don't require to look good, it's rather an activity to just train my brain doing it, will I ever look back on them after finishing a page?

If it should look good I'd rather go out of my way and typeset it in LaTeX, but that is not the point here. So why the whole hassle?


## Step two: remembering a blog-post
Due to a conversation about using a drawing tablet for video confereces I recalled having read something of the late mathmatician Gilles Castel in his post: [My Mathematics PhD research workflow](https://castel.dev/post/research-workflow/#handwritten-digital-notes). I will probably come back to exactly this post later this year when I'm once again revamping the technical side of my workflow, but for now we'll focus on the handwritten notes part of it.

Used here is xournal, which is now proceded by xournalpp. Further, it appears one can easily duplicate, move stuff around and get to the point. Not having to spend most the time on rewriting equations but just the small parts that changed during operations, freeing some seconds that would've gotten wasted at a rather useless step (mathematically).

At last we see one thing that is perhaps a little shocking to the dear vim user, while one can use the pen to draw and alike, one also has to use the pen to select color, thickness, tool, out of bars that are on the sides. Once again, we can spot seconds that get lost.

At this step I already got out an old "Wacom Bamboo Graphic Tablet" of my dad and knew I had to try around with it, what I could adapt, change up and make more effective.


## Step three: first impressions
{{< figure src="../../handwritten/xournal-ui.png" title="Figure 2: Xournalpp UI" >}} 

First the software side of it. Xournalpp seems great, there are very cool and useful tools and it is pretty customizable, at least the bars, where they are, ...

I got a bit disappointed because the premapped hotkeys were e.g. <kbd>strg+shift+p</kbd> to switch to a pen, and then it struck me, there were no setting where one could set hotkeys!

All the other hotkeys were set in familiar fashion and it appears rather useless to me, because hotkeys are to make life easier and fun, enabling one to spend it on worthwhile activities instead of clicking with the mouse. But that didn't work out here. 

Would I further have used the standard hotkeys I'd have carpal tunnel syndrome before selecting the eraser tool when being done with the pen!

*You could argue that that's exagerated, but you could also just agree.*

## Step four: how do I set hotkeys?
I queried their issues for some time and have not found a very satisfactory answer, lots of people seem to use flypie or other odd things. Some time later I found a plugin on gitlab [xournalpp-shortcuts](https://gitlab.com/FabianUntermoser/xournalpp-shortcuts), that was in total nothing else than the goldmine of an [issue here](https://github.com/xournalpp/xournalpp/issues/919), but probably the condensed format helped me to understand it.

There I was, happy to have found an answer, that there is a possibility, even if not the easiest way forward. 

They have an API for plugin devs and here the [documentation for it](https://xournalpp.github.io/guide/plugins/plugins/).
The API is in lua[^1] which is cool cause I accidentally learned that[^2] while figuring out neovim.

So I was trying to understand the API, what of it I actually needed (basically just `app.uiAction`) and how to modify which file to make things work. 

Just while writing this I have also found [an incredible file](https://github.com/xournalpp/xournalpp/blob/1002c131e1d7a1cb1243d955c611979b7faec488/src/enums/generated/ActionType.generated.cpp) in the above mentioned issue to figure out `app.uiAction` names.

So this step is done, I just add functions to the `main.lua` and mention them in the top of the file in another function which adds hotkeys to them. 

#### snippet out of my config to illustrate
```lua
function initUi()
  app.registerUi({["menu"] = "Pen Tool", ["callback"] = "pen", ["accelerator"] = "m"});
  app.registerUi({["menu"] = "Cycle through line style", ["callback"] = "linestyle", ["accelerator"] = "<shift>m"});
end


function pen()
  app.uiAction({["action"] = "ACTION_TOOL_PEN"})
  print("ACTION_TOOL_PEN: selected")
end


local linestyleList = {"PLAIN", "DOT"}
local currentLinestyle = 1

function linestyle()
  currentLinestyle = currentLinestyle % #linestyleList + 1
  app.uiAction({["action"] = "ACTION_TOOL_LINE_STYLE_" .. linestyleList[currentLinestyle]})
  print("ACTION_TOOL_LINE_STYLE_" .. linestyleList[currentLinestyle])
end
```

The whole mess you can find [here](https://github.com/d-rens/dotfiles/blob/master/xournalpp/plugins/shortcuts/main.lua).


## Step five: how will I set hotkeys?
As I've figured out how to set the hotkeys I'll continue making up a plan for it.

Below you can see how it has turned out. As I use a split keyboard talked about in the [Dactyl post](../dactyl), it makes sense to use one hand exclusively for the mapping. As I'm right handed, using the right hand to write, I'll just use the left-hand keyboard side to be able to have the left hand constantly on the keys and the right one on the pen.

Also I am using just the base and shift layer, shift because that is on the left side on the keyboard, so accessible easily.

It ended up so that half of the keys get mapped to letters that make sense such as `s -> select region` and `S -> select rectangle` but the other half gets in result mapped to letters that were left over as e.g. `t -> save` and `T -> save to pdf`.

The Boxes marked red are already hard-set in the program, luckily to similar things as I'd have mapped them myself by them being some important vim keys.

{{< figure src="../../handwritten/hotkeys.jpeg" title="Figure 3: The plan to set hotkeys" >}} 

Currently there are two problems left, that I will probably figure out in the next days.
1. The functions for undo + redo won't work, no idea why.
2. I can't use the shift layer of the numbers, the functions work on other keys but I need to have them there. Probably a misunderstanding of mine about how to declare the keys in lua. Normally `<shift>f` would work to say `F`, but here for the numbers `<shift>1` does not work, nor `<shift>!` or `!`. Will also be figured out at some point and then pushed, if you have any idea to fix it let me know.


## Conclusion

While it is not as nice to write on a tablet, it's not neglectable that it's able to be more effective. Thus, I will use it for some more weeks while preparing on some final exams. I see upsides mainly for math, there is no good reason to e.g. write with a pen normally on it, there a keyboard will be far superior.

Further, while the system is yet very nicely optimized, my usage of it has not. That will just take some more weeks, will update on it.

### update: 11th April
To start of, it works really well. 
But as the tablet I was using was an old model having a nearly broken pen and small drawing area, making it harder to do any specific notation, without zooming before, I decided to look out for newer models, ending up on the Wacom one in medium size, getting it as warehouse deal for 40 euros.

The bigger drawing area is helpful and it's design wise pleasingly minimalistic. In the following you can see the now updated pen drawing.

{{< figure src="../../handwritten/new-pen.png" title="Figure 4: New pen + hotkeys on it" >}} 

As seen below, the tablet's drawing area is pretty big, 13,5cm x 22,6cm, but it is pretty helpful for the small notations to do.

{{< figure src="../../handwritten/setup.jpg" title="Figure 5: Setup" >}} 


### dwm hotkeys
About the hotkeys within xournalpp I have talked plenty but they also live outside of it in my system, currently I have a bash function, mapped to `alt+x`, to open a xournalpp file `note.xopp` in a folder named the current date, e.g. `2024-04-11`, the folder structure within a `~/folder/notes/` directory them seems the following:
```
.
├── 2024-03-28
│   └── note.xopp
├── 2024-03-29
│   └── note.xopp
├── 2024-03-30
│   └── note.xopp
├── 2024-03-31
│   └── note.xopp
.
```

This is also taken out of Castel`s "phd workflow", if I create a TeX file on the following day with `alt+n`, then it puts this TeX file also within this folder.

I will need to think about how to adjust this to my needs. If I don't talk daily TeX notes with the results of the days handwritten notes, due to not doing research, then it's not really conclusive, rather a scrap paper alternative. My current mathematical learning is nothing else than learning with scrap paper, but it won't be a good way without reflecting on the results, ..

You get the point, that's still to be worked out in the following weeks, but at the moment I am happy with the workflow, despite knowing how much better it could be or result to be.




[^1]: Brazil mentioned
[^2]: Fun fact, nobody has ever tried to learn lua, you just accidentally know it at some point[^3].
[^3]: I'm joking
