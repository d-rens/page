---
title: "NixOS Series, Part 1, Introduction"
date: 2024-09-22T00:00:00
tags: ['linux']
description: First post of the nixOS series.
---

If you are like me, you probably spent too many hours configuring operating
systems, sometimes to just get things to work or to have to press just one less
button to achieve things during other times to just look good.

For me there always stood one elephant in the room, which was the amount of time
I spent on it.

As an example, when using arch, there were occasionally problems that I had to get
fixed by going through a multitude of arch-wiki posts where eventually somebody
put a command that would fix it.
You will always be able to find a solution that way due to the great community but
eventually I came to the conclusion that this is a very unsustainable process.

When you use multiple machines, say for work/private, then you can't just have the
exactly same installations on multiple machines, at least not when you value your
time.

You can easily transfer your dotfiles, but what about:
- users
- groups
- DE/WM/greeters
- services
- /etc/ settings
- secrets
- browser
- audio
- partitioning
- boot-loader
- packages

## solution

But that is a problem lots of people face, so there is already a solutions which
is just to declare the whole operating system. Of those there exist at least two
big ones, there is nixOS, declared in the functional nix language and GNU Guix,
written in scheme.
I was familiar with neither of those languages, but two friends urged me to give
nixOS a try and scheme scared me, so it was a easy decision which of those to
give a try.

So my journey has started. I was stuck in final exams when I made the decision
so I needed to wait a bit, letting the ideas what all to do grow on me. At that
point I thought I could maybe spend some days with it but I did not expect what
was to come.
On the day I have written my last exam of the year I went home, put the nixOS
ISO on a Ventoy stick, got an old Thinkpad x220 out of a cabinet and started
going through tutorials.

I was soon fascinated but saw there were a lot more things to be done, and as
I kept spending time with it I just kept finding more and more things to do.

## nixOS post series

Given all the practical things I've learned throughout this time I've decided to
write about the process here. To introduce you to the matter and more
importantly explain specific parts of my configuration where often I wished
there was more documentation around or just examples.

I'll structure the posts the following:
1. system side
2. flakes
3. home manager
4. individual programs:
   1. borg (backups)
   2. sops (secret management)
   3. stylix (styling)
   4. nixos-anywhere (remote installation)
   5. disko (partitioning)
   6. keyd (remapping keyboard)
   7. neomutt (mail)
   8. syncthing (syncing files locally)
   9. wireguard and maybe openvpn (vpn)
   10. fish (shell)
   11. nixvim (text editor)
   12. firefox

My current configuration you'll be able to find on
[sourcehut](https://git.sr.ht/~d-rens/nixos-dotfiles/).

If you have any specific topics you'd like to be brought up just reach out via
email at [contact](/about/#contact).

