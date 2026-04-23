all: clone.png push.png pull.png git_areas.png

../%.png: %.pdf
	magick -density 192 $^ $@

%.pdf: %.tex
	pdflatex $^
	rm $*.aux $*.log

clean:
	rm *.pdf *.png
