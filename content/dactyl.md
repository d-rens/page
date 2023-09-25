---
title: "Dactyl"
date: 2023-09-21T08:31:14+02:00
lastmod: 2023-09-21T15:31:14+02:00 
tag: technology
draft: true
---

# The Dactyl Experience

## Preface 
During the last days and weeks I've spend some of my time soldering,
configuring and figuring about a dactyl keyboard. Now it is done and I can now
type much more ergonimic and better than I could before, in the following I
will talk about the process and maybe you can get something out of it :).

A dactyl - or dactyl manuform - keyboard is a parametric generated keyboard
with the following ergonomic features to make it great to use:

**Split**
: Allows one to keep the hands on shoulderwidth or further which makes it
  convenient to use over long time.

<p>&nbsp;</p>

**Staggered Columns**
: If you look at your keyboard the rows are most likely staggered, if you then
  look at your hands you see they are indeed not staggered horizontally but
  vertically. For clarification, there was a use for the staggered rows back in
  the ages of typewriters due to how they were constructed, but now many decades
  later we still carry the technical dept around with us [^1] *(that's like if
  one were to use windows).* 

<p>&nbsp;</p>

**Thumb cluster**
: One of the things I still got very annoyed at after many years of typing is
  the following:

    - Two pinkies are supposed to handle ~24 keys together.
    - Two thumbs are supposed to handle 1!
: This I would argue is inherently nonsense. The pinky's range of motion is
  biologically-wise the most restricted and weak, whereas the thumbs range is
  bigger and able to be multiple times stronger [^2].

: So the dactyl features a thumbcluster of six keys, in some later section I
  will again mention it in my thoughts on the layout I made.



## Building

### Parts

**3d-printed** 
- case l & r
- bottom plate l & r
- structure to hold Arduino-Pro-Micro, reset switch and 3,5mm jack socket

**To be bought**
- cables (cabels I've used were extracted out of 1,2m network cable)
- around 80 switches
- around 80 keycaps 
- two Arduino-Pro-Micros
- two extra switches to reset the Pro-Micros
- jack cable (size variable to fit your need)
- twelve threaded inserts


## Preparing

### Printing
To print the case with bottomplate one needs to setup a clojure environment
which than takes parameters to calculate the model as SCAD file. To figure the
clojure part out I've used (this tutorial)[https://youtu.be/CxNKWNKBLMs?si=DzsP05Oc1_6IBStr].

When clojure has calculated the model one can open it in SCAD, render it and
save the .stl which can than be handled by a slicer. I used Ultimaker Cura for
this step but it does not matter which one is used. 

The printing took two times 16 hours for cases and two times 5 hours for the plates. 

Cleaning up the print took together around 2 hours, the cases had some annoying
spots where one had to remove support.

### Soldering
















<!--```sh
$ qmk flash -kb handwired/dactyl_manuform/5x7 -km my-map
```-->


[^1]: One could argue here that a layout change from qwerty/qwertz to something
      like dvorak would solve another huge issue with typewriters. Yes, expect a
      post on this the next weeks. 

[^2]: I did not found science backing this, but in my head it makes a lot of
      sense, so you might as well trust me on it.

[^3]: The 3d-printed parts are on [my dactyl-manuform
      repo](https://github.com/d-rens/dactyl-manuform) it's a fork of the
      dactyl-manuform which is a form of the dactyl-manuform-mini-keyboard
      which is a fork of the dactyl-keyboard (manuform) which is a fork of the
      original dactyl. Minor instructions on how to change parameters, render
      it with clojure and scad, etc. are attached.

