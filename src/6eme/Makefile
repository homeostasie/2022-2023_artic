# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/4eme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 6x1-fraction-partage/*.ipe 4x6-Pythagore/*.ipe 4xbb/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

6x1-fraction-partage/%.pdf: 6x1-fraction-partage/%.ipe
	ipetoipe -pdf $<


1ie:
	pdflatex 6x1-fraction-partage/6x1-ie.tex
	pdflatex 6x1-fraction-partage/6x1-ie.tex
	mv 6x1-ie.pdf '$(PDFDIR)'/6x1-ie.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~