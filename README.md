T<sub>E</sub>XB<sub>R</sub>E<sub>W</sub>
=======

An attempt to make good-looking homebrew documents for various
roleplaying systems (currently only D&D 5e), using
X<sub>Ǝ</sub>T<sub>E</sub>X for typesetting.

Unless otherwise specified, all documents are released under the
WTFPLv2. See the `COPYING` file for more details.

Some of the assets are released under different licenses. See the
`CREDITS.tex` files for more details.

Demos
=====

* **For D&D 5e: https://artefact2.github.io/texbrew/dnd-5e/skel.pdf**

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

* part pages
* overflowing art
* proper footer marks
* fix bugs
* remove background dependency, use everypage instead, remove overlay from textpos
