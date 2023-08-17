---
title: "Workflow"
date: 2023-07-26T12:10:19+02:00
mod: 2023-08-09T12:10:19+02:00
tags: ['technology']
---

# goals of the setup
The goal of the workflow is to be ever evolving to be more efficient and
useful. The main application is to write LaTeX, manage references,
figures, etc. So that one does not need to think about it anymore but
has a good experience using it and optimal output.

## [LaTeX](https://en.wikipedia.org/wiki/LaTeX)
LaTeX is a typesetting software that makes digital typesetting easy and
visually appealing. However, there is a little entry barrier because you
need to know commands to use it. Nevertheless, everything is generally
logical and makes sense.

Personally, I have a lot of fun using it, and it often motivates me to
get work done instead of being a hindrance like Word. I don\'t want to
focus solely on why Word is bad, but here\'s a nice way to compare them:
In Word, you set your text while typing, and you only see the
\'finished\' text. Consequently, while writing, you might do it
naturally or, to procrastinate, start to format everything. Then, when
you move a figure, there is the possibility that everything gets messed
up.

On the other hand, with LaTeX, you just write in plain text using, for
example, Vim (which also makes it more enjoyable to use). You see the
text with commands within it, and you focus on writing content without
worrying about how it looks. When you want to add a footnote, you simply
use \'\\footnote{}\' and input the content. There are no style
considerations to think about, but it still yields a sense of logical
structure, resulting in the best and most perfect outcome from my
experience.

Another thing, things like bibliographies are made nearly automatically,
I luckily have never written a bibliography myself, but seeing people
actually doing it, or \'just\' copying it from somewhere for every
single citation they have seems most horrible.

## [Inkscape](https://inkscape.org/about/)
Inkscape is a vector tool used for creating and editing vector graphics.
I use it with LaTeX to make some of my mathematical figures. It\'s
open-source, which is appealing, and it\'s also extensible. As
extensions, I use a figure manager that seamlessly integrates with LaTeX
without any extra thinking. Additionally, I use a shortcut manager that
allows me to have different stroke strengths, fill colors, arrow
endings, etc., readily available with just a keystroke in the app. This
convenience reduces the need for excessive mouse usage.

## [Neovim](https://github.com/neovim/neovim)
Neovim is my text editor of choice for several reasons:
- Firstly, it\'s more extensible and easier to understand than Vim (for this article: vim = neovim).
- Secondly, Vim is highly efficient once you learn it.

Vim maps every letter on the keyboard, and while non- and capitalized
letters require certain keys to enter insert mode for writing text, as
long as you are not in insert mode, you can navigate and edit a text
file or document using the entire keyboard. This allows for faster
editing compared to any other text editor. Admittedly, it takes some
time to get used to, but the skills I\'ve gained from learning Vim have
been tremendously beneficial, as mentioned in the LaTeX section.

It\'s a lot of fun to use.

## [Zotero](https://www.zotero.org/)

Zotero is one of the programs I enjoy less due to its heavy GUI-based
nature. However, its convenience makes me continue using it, which
speaks highly of its usefulness.

Zotero is a reference management software used to gather references such
as papers, articles, books, etc., for academic research. It allows users
to view, annotate, export bibliography citations, and perform other
functions.

Personally, I use Zotero for three main purposes:

-   Using the browser extension to add sources with just one click.
-   Automatically writing all citations into a .bib file every two seconds for BibLaTeX to use.
-   Being able to cite these sources in LaTeX without any problems or hassle.

## [Obsidian](https://obsidian.md/)
Lastly, I use Obsidian because I did not have a good system to take care
of my plain-text notes. Obsidian seems to be a good alternative.

But I do use it fully in Neovim with a plugin, so it is enjoyable to
use. Here are some features which I enjoy:

-   Write everything in markdown.
-   Have automatically daily notes (accessible with a hotkey in my config).
-   Reference different notes.
-   Show a graph to display links between notes.
-   Use templates.

# conclusion
There is one initial problem I have with the setup, which is the setup
is perfectly optimized to write papers and do reasearch, but at the
moment I have as good as nothing to do with that.

This is the taking notes part of the setup, later in Part 2 I\'ll talk
abuot the bigger system: tiling window manager, hotkey deamon, etc.

If you have any questions, ideas or other things you want to mention,
you can contact me at:

[*contact@d-rens.site*](mailto:contact@d-rens.site?subject=Web%20page%20contact%20link).



### references
1. [dotfiles](https://github.com/d-rens/dotfiles)
2. [inkscape-shortcut-manager](https://github.com/d-rens/inkscape-shortcut-manager)
3. [LaTeX](https://en.wikipedia.org/wiki/LaTeX)
4. [Inkscape](https://inkscape.org/about/)
5. [Neovim](https://github.com/neovim/neovim)
6. [Zotero](https://www.zotero.org/)
7. [Obsidian](https://obsidian.md/)

### updates
This will this be constantly updated, the things you can expect to get
added soon are:
-   tmux
-   zettelkasten for notes
