IMAGES := clone push pull git_areas

all: $(IMAGES)

$(IMAGES): %: ../%.png

../%.png: %.pdf
	magick -density 192 $< $@

%.pdf: %.tex
	pdflatex $<
	rm -f $*.aux $*.log
