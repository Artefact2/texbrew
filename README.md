T<sub>E</sub>XB<sub>R</sub>E<sub>W</sub>
=======

An attempt to make good-looking homebrew documents for various
roleplaying systems (currently only D&D 5e), using
X<sub>Ǝ</sub>T<sub>E</sub>X for typesetting.

Unless otherwise specified, all documents are released under the
WTFPLv2. See the `COPYING` file for more details.

Some of the assets are released under different licenses. See the
`CREDITS.tex` files for more details.

Motivation
==========

Why create something like this? Well, T<sub>E</sub>X was *made* to
typeset documents with perfection. As such, it takes care of difficult
things such as:

* Correct page layout (left/right pages have different margins, chapters always open on a right page, etc.);
* Handling page breaks properly (even with multi-column text);
* Handling floating things (narrow or wide) and placing them appropriately;
* Keeping track of things (table of contents, references, appendices, etc.);
* Good pagination, marks, etc;
* And many other things we don't even think about (like autoadjusting spaces to avoid widows and orphans).

Why use X<sub>Ǝ</sub>T<sub>E</sub>X ? For one, it is modern (unicode
support out of the box) and makes it easy to use custom OpenType
fonts (with fontspec).

Demos
=====

* **For D&D 5e: https://artefact2.github.io/texbrew/dnd-5e/skel.pdf** ([draft version](https://artefact2.github.io/texbrew/dnd-5e/draft-skel.pdf))

Usage
=====

To compile the demo document:

    cd dnd-5e
    make skel.pdf
    # Or: make draft-skel.pdf for a draft version (faster, no graphics)

To start your own document:

    cd dnd-5e
    cp skel.tex mybook.tex
    $EDITOR mybook.tex
    make mybook.pdf
    # Or: make draft-mybook.pdf

Todo
====

* overflowing art
* [fix XXXs](https://github.com/Artefact2/texbrew/search?utf8=%E2%9C%93&q=XXX)
* fix bugs
