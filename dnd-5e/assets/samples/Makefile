BPG=$(shell find . -type f -name "*.bpg")
PDF=$(patsubst %.bpg, %.pdf, $(BPG))

all: $(PDF)

%.bpg: %.png
	bpgenc -o $@ -q 29 -m 9 $<

%.pdf: %.bpg
	bpgdec -o $@.png $<
	convert $@.png -background white -alpha remove -alpha off $@-rgb.jpg
	convert $@.png -alpha extract -colorspace GRAY -negate $@-a.jpg
	pdflatex -halt-on-error -jobname=$@ "\def\pxwidth{`identify -format '%w' $@.png`}\def\pxheight{`identify -format '%h' $@.png`}\def\themask{$@-a.jpg}\def\theimage{$@-rgb.jpg}\input{mask.tex}"
	mv $@.pdf $@
	rm $@.log $@.aux $@.png $@-rgb.jpg $@-a.jpg

.PHONY: all
