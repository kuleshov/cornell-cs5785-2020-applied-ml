#LECTURES:=lecture1 lecture2 lecture3 lecture4 lecture5b lecture6

NOTEBOOKS:=$(wildcard *.ipynb)
SLIDES:=$(subst ipynb,slides.html,$(NOTEBOOKS))
HTML:=$(subst ipynb,html,$(NOTEBOOKS))
PDFS:=$(subst ipynb,pdf,$(NOTEBOOKS))

$(SLIDES): %.slides.html: %.ipynb
	jupyter nbconvert $< --to slides --reveal-prefix "http://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.3.0"

$(HTML): %.html: %.ipynb
	jupyter nbconvert $< --to html_embed --reveal-prefix "http://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.3.0"

$(PDFS): %.pdf: %.ipynb
	jupyter nbconvert $< --to pdf --reveal-prefix "http://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.3.0"

notes:
	make $(HTML)

slides:
	make $(SLIDES)

pdfs:
	make $(PDFS)

clean:
	rm *.html *.pdf

all:
	make notes slides pdfs
