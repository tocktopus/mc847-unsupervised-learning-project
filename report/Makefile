MAIN = main
LATEXMK = latexmk

.PHONY: all clean

all: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex refs.bib $(wildcard sections/*.tex)
	$(LATEXMK) -pdf -interaction=nonstopmode -halt-on-error $(MAIN).tex

clean:
	$(LATEXMK) -C $(MAIN).tex
