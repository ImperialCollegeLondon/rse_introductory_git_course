IMAGES := clone push pull git_areas

all: $(IMAGES)

$(IMAGES): %: ../%.png ../%-dark.png

../%.png: %.pdf
	magick -density 192 $< $@

%.pdf: %.tex
	sed 's/@@COLOUR_VAR@@/black/g' $< | pdflatex -jobname=$*

%-dark.pdf: %.tex
	sed 's/@@COLOUR_VAR@@/white/g' $< | pdflatex -jobname=$*-dark
