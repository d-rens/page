---
title: "Programs"
date: 2024-01-13T19:47:06+01:00
description:
tldr: "On this page I'll list what software and hardware I use and why."
tags: ['software', 'hardware', 'linux']
---

# Why is it worth talking about programs?
I have been on windows for most of my time, then switched to macos on an m1 macbook because I lost interest in playing games so there was no reason any more to stay on windows. 
Within the first half year of using macos I discovered LaTeX, due to that I have also found [Luke Smith](https://lukesmith.xyz/) what made me fall deep into the software-minimalism rabbit-hole.

First I have used [asahi linux](https://asahilinux.org/) on the mac but due to not being able to use speakers, microphone, display under 100% brightness and some other limitations I finally got an used Thinkpad and installed archlinux. I have switched distros some times but always came back to arch. It took some time to figure out and become productive on, but now, not even one year later I have figured out a setup that is pretty minimalistic in the sense that most things run in the terminal and are written efficiently.

Naturally that also got into self hosting things which I'll talk about in the end of this site.

## meta

Operating system
: **Archlinux** it is minimal and just works (and if not one can easily fix it).

Terminal
: **st** is the suckless simple terminal, with the ligature and alpha patches.

Window manager
: **dwm** suckless' "dynamic window manager", for some reason I've used bspwm before a long time, but suckless had the bspwm features and much more. Just as **st** and every other suckless program it is written in C, one compiles it oneself and can edit what one wants to be changed or just write new features. As statusbar I use dwmblocks.

Text editing / programming
: **Neovim**, a more modern fork of vim that suports lua, highly extensible and does not require a mouse.


## utils

rss
: **newsboat**, very simple rss/atom reader written in C++.

music player
: **ncmpcpp with mpd**, I've used cmus for a while but it was too primitive and I used streaming instead most of the time. Once I switched to ncmpcpp with mpd as backend I have not looked back. It has a very convenient tag editor, vim bindings and every feature one could wish for.

video player
: **mpv**, just works.

file browser
: **lf**. Have used ranger in the past but couldn't morally use it with python, lf most of the features ranger has but is written in go and easier to use.

mail
: **neomutt with abook**, I have for too long not cared about mail and just used it where I had to due to weird web-uis and more things to click than to type. With neomutt one has vim-like bindings and the mails are written in vim, it is just as simple as email needs to be, there is no option to use a mouse and it is highly customizable. abook then manages the contacts so one does not have to remember everybodys address, just the name. abook is even simpler and also working within the terminal from there one can open neomutt with the sender already input in the right field and prompted with entering the subject.


## producing

documents
: **LaTeX & rmarkdown**. Since I have used LaTeX for the first time it was a lot of fun, now I use it for letters, academic papers and everything that needs to be printed and typeset correctly. If I need to write papers that have code or want to print code I use rmarkdown, it exucutes code on compile time and supports R, python, SQL and some other languages with knitter, it is very helpful when doing data analysis and it just renders the code after codeblocks to either just get the output or graphs that get output.

presentations
: **LaTeX beamer**, makes the most sence to use when already using LaTeX for the documents, one can just paste things from one to the other and on this way migrate things with the same markup, pictures...

data analysis
: **python or R**, I know both not enough to make my mind up on what to use.

pdf
: **zathura**. Minimalist pdf viewer with vim-like bindings, options for double-page view and inverted colors.

image viewer
: **nsxiv**, just works, has many nice options, e.g. thumbnail view or printing the selection to stdout.

image modification
: **gimp**, on non linux systems the affinity suite.

## misc

monero
: **monero-wallet-gui**, just works.


# hardware
laptops
: thinkpad T470 as daily driver, X220 as distraction free alternative.

tablet
: boox tab ultra, an eink tablet for reading websites, textbooks or books.



