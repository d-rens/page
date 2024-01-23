---
title: "Layout"
date: 2024-01-23T22:14:50+01:00
tags: ['technology', 'software']
description: Changing the keyboard layout from qwerty to semimak-jq. Process and review of the process.
tldr: The following will be the way I came to change my layout and the process/thinking behind it, ending with thoughts on it.
---


# Step One -- Realisation
Having typed all my life on qwerty or qwertz I got used to it. I got into
practising typing to gain speed and accuracy, towards the end I averaged around
90 words per minute (wpm) and had a accuracy of >95%. 

But at some point I got fed up with it, why did I still use the normal layout?
That has no reason for existing any more and that after I have switched to
a tiling-window-manager, vim and countless other things, just to get the last 
seconds off the clock and have the computer do whatever I want it to do as 
fast as possible. 

There was always the one interface for human-machine connection and it did not
make sense.

Morally I could not do it any more, seeing words like "minimum" just using two
fingers going up and down all the time, "typewriter" not having a single key
on the home-row[^1] and countless other things including strain in the hands.

You get the point, after a whole bunch of general optimisation there now was 
time to change the keyboard layout.


## Step Two -- What Now?
So I came to the realisation, but what was I going to change to now? I have no
idea about keyboard layouts so I figured I know the Dvorak layout, and that sounds
interesting. Just at the time I was also writing my [last post](../dactyl) about 
the Dactyl keyboard so I was already in one community where I knew people to ask,
but I didn't, instead I spent a week learning Dvorak, for sake of one less thing 
to browse for you, here is the Dvorak layout:
```
--------- Dvorak --------
' , . p y f g c r l ? + |
 a o e u i d h t n s -
  ; q j k x b m w v z
```
What I found the most interesting is the position of the punctuation keys, I 
enjoyed the idea of them finally being elsewhere, so why not there. Save to say
I did not think too much about it, just used it.

Some days later then I have send a picture into the monketype-discord[^2], with
my then finished keyboard, the key-caps being in the Dvorak layout. I probably 
said something about using Dvorak and then got told by two people that appeared 
to know what they are on about to not use Dvorak, I did not have a reason to use
it in the first place so I was willing to listen. What I got told to use instead 
was "Semimak[^3]" or more specific Semimak-jq[^4] which is an updated version,
in the footnotes I have added the authors blog posts about it if you want to
read more into it. Here is the layout:
```
------ semimak-jq -----
f l h v z ' w u o y [ ]
s r n t k c d e a i ; \ 
  x j b m q p g , . / 
```
I have then also found the alt(ternative)-layout community, that is a bunch of 
people all being into developing keyboard layouts themselves, optimizing others 
and alike, somehow I managed to not fall into that rabbit-hole myself and ended 
up just taking out of there what was offered to me. 


## Step Three -- Learning
As already said, first I spend a week learning Dvorak and just then switched to 
what I use now. In the graph you can see that very nicely, let me point out the
individual peaks in it.

1. Cut off peak in the beginning: the last tests on qwerty with a normal keyboard.
2. First full peak: using the [Dactyl](../dactyl) keyboard with qwerty.
3. Small blob at the bottom afterwards: Dvorak
4. Gradual slope starting at 1/3: Semimak-jq

{{< figure src="../../layout/progress.png" title="Progress on Monketype" >}} 

> The variance at the end is due to testing around with harder tests, I luckily 
am not this unsteady. 

The first test with Semimak-jq was on the 15th October 2023, today it is the 23th
of Janurary 2024, three months have passed and I am as good as back on my old speed
just much more ergonomic with a type-friendly layout.

To add some date just for the typing with Semiak-jq in dedicated learning on
monketype.com, excluding any other practice and day-to-day typing.

| measure | value |
| ------- | ---- | 
| estimated words typed | 20061 |
| tests completed | 507 |
| time typing | 8:47h |
| highest wpm | 93 |

I am not most happy with those results, but am far from at the end of the typing
journey, I hope I won't stagnate any time soon. Currently there are some people using the layout with scores around [200 wpm by the author](https://semilin.github.io/blog/2022/final_reflection_on_semimak.html) up to [238 wpm by fenno](https://www.youtube.com/watch?v=-8F-xIah79w). Those are incredible numbers and I would hope to reach steady 150, but I will see about that the following months.


## Step Four -- Review the Process, Answer Questions
> What has been good? 

- It has been easy on my fingers, the layout is specifically optimated to have
the most used keys on the home-row or at least on a reasonable position to use. 
- Good has also been to not have issues with the keyboard layouts reasonableness any more and just uses it instead[^5].

> What has not been optimal? 
- Not practising it deliberately enough, if I would have spend two more weeks
  at the start just doing typing tests for 30 minutes a day it would have
  helped to start off faster.

> Does it deserve being as intriguing as it seems to be?
- Not at all, I was scared to do the change but once I did it I stopped looking back
it does sound intriguing, very much so, but it is not. One just requires a lot of 
patience and not reason oneself back into using the old. For me the very easy
argument was the following "If I type for the rest of my life, that might be 80
years, then I surely want not to spent that on qwerty because I was too lazy at
the start to just spend a quarter year to learn something different that makes
more sense.

> Most importantly, how does one use vim?
- There are people completely remapping things so actions are at the old positions
but I find that to be unnecessary complex, instead I have not changed any setting 
regarding the layout in vim and still been able to happily use it.

> How does one set different layouts
- Linux: I just use xmodmap
- macos: Ukulele
- Windows: no idea

> Can I recommend to switch away from the just-works option? 
- Yes, very much so, It has not to be Semimak, as said, I don't have much
  reason to use it myself, there are plenty of other alt-layouts that are
  interesting and maybe even better, e.g. for German there is the "neo" layout,
  and for other languages probably other specific layouts. But save to say
  I encourage you to just use something else than qwerty. It is not any different
  than say switching to vim when coming from an IDE, unusual but most definitely 
  worth the learning.




[^1]: The "home-row" is the middle row, probably `asdfgh...` for you.
[^2]:
[^3]: [post about the layout by the inventor](https://semilin.github.io/blog/2021/semimak.html)
[^4]: [next post by the inventor about it needing updates](https://semilin.github.io/blog/2021/reflection_on_semimak.html)
[^5]: I am sorry if this posts leads you towards this agonizing pain.
