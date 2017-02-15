INCLUDES=$(shell find . -type f -name "*.tex")

draft-%.pdf: %.tex $(INCLUDES)
	xelatex -halt-on-error -jobname=`echo $@ | rev | cut -b5- | rev` "\def\isdraft{1}\input{$<}"
	xelatex -halt-on-error -jobname=`echo $@ | rev | cut -b5- | rev` "\def\isdraft{1}\input{$<}"

%.pdf: %.tex $(INCLUDES)
	xelatex -halt-on-error $<
	xelatex -halt-on-error $<

clean:
	rm -f *.{aux,log,pdf,nav,out,snm,toc}

.PHONY: clean
