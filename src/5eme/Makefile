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
FIGSRC = $(wildcard 5x2-geometrie-quadrillage/*.ipe 4xbb/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

6x2-geometrie-quadrillage/%.pdf: 6x2-geometrie-quadrillage/%.ipe
	ipetoipe -pdf $<

# Chapitre 1

1ie:
	pdflatex 5x1-calculs/5x1-ie.tex
	pdflatex 5x1-calculs/5x1-ie.tex
	mv 5x1-ie.pdf '$(PDFDIR)'/5x1-ie-calculs.pdf

2ie:
	pdflatex 5x2-geometrie-quadrillage/5x2-ie.tex
	pdflatex 5x2-geometrie-quadrillage/5x2-ie.tex
	mv 5x2-ie.pdf '$(PDFDIR)'/5x2-ie.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
