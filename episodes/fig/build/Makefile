.PHONY: clone push pull git_areas all

clone: ../clone.png
push: ../push.png
pull: ../pull.png
git_areas: ../git_areas.png

all: clone push pull git_areas

../%.png: %.pdf
	magick -density 192 $< $@

%.pdf: %.tex
	pdflatex $<
	rm -f $*.aux $*.log
