# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/5eme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 5x2-symetrie-centrale/*.ipe 5x3-triangles/*.ipe 5x4-relatifs/*.ipe 5x5-aires-et-perimetres/* 5x8-angles/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

5x2-symetrie-centrale/%.pdf: 5x2-symetrie-centrale/%.ipe
	ipetoipe -pdf $<
5x3-triangles/%.pdf: 5x3-triangles/%.ipe
	ipetoipe -pdf $<
5x4-relatifs/%.pdf: 5x4-relatifs/%.ipe
	ipetoipe -pdf $<
5x4-relatifs/%.pdf: 5x4-relatifs/%.ipe
	ipetoipe -pdf $<
5x5-aires-et-perimetres/%.pdf: 5x5-aires-et-perimetres/%.ipe
	ipetoipe -pdf $<
5x8-angles/%.pdf: 5x8-angles/%.ipe
	ipetoipe -pdf $<

# Chapitre 1

1ie:
	pdflatex 5x1-calculs/5x1-ie.tex
	pdflatex 5x1-calculs/5x1-ie.tex
	mv 5x1-ie.pdf '$(PDFDIR)'/5x1-ie-calculs.pdf




# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
