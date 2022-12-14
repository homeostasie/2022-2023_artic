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
FIGSRC = $(wildcard 4x3-triangles-semblables/*.ipe 4x5-pythagore/*.ipe 4xbb/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x3-triangles-semblables/%.pdf: 4x3-triangles-semblables/%.ipe
	ipetoipe -pdf $<

4x5-pythagore/%.pdf: 4x5-pythagore/%.ipe
	ipetoipe -pdf $<

4xbb/%.pdf: 4xbb/%.ipe
	ipetoipe -pdf $<

dm3:
	pdflatex 4x0-DM/4x3-dm-appolo.tex
	pdflatex 4x0-DM/4x3-dm-appolo.tex
	mv 4x3-dm-appolo.pdf '$(PDFDIR)'/4x3-dm-appolo.pdf
1ie:
	pdflatex 4x1-relatifs/4x1-ie.tex
	pdflatex 4x1-relatifs/4x1-ie.tex
	mv 4x1-ie.pdf '$(PDFDIR)'/4x1-ie-relatifs.pdf

2ie:
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	mv 4x2-ie.pdf '$(PDFDIR)'/4x2-ie-proportionnalite.pdf

4exo:
	pdflatex 4x4-notation-scientifique/4x4-exo.tex
	pdflatex 4x4-notation-scientifique/4x4-exo.tex
	mv 4x4-exo.pdf '$(PDFDIR)'/4x4-exo-puissances.pdf

4ie:
	pdflatex 4x4-notation-scientifique/4x4-ie.tex
	pdflatex 4x4-notation-scientifique/4x4-ie.tex
	mv 4x4-ie.pdf '$(PDFDIR)'/4x4-ie-puissances.pdf

5ie:
	pdflatex 4x5-pythagore/4x5-ie.tex
	pdflatex 4x5-pythagore/4x5-ie.tex
	mv 4x5-ie.pdf '$(PDFDIR)'/4x5-ie-pythagore.pdf

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
