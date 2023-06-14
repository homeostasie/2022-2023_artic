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
FIGSRC = $(wildcard 5x2-geometrie-quadrillage/*.ipe 5x4-symetrie/*.ipe 5x5-triangles/*.ipe 4xbb/*.ipe 5x8-aires/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

5x2-geometrie-quadrillage/%.pdf: 5x2-geometrie-quadrillage/%.ipe
	ipetoipe -pdf $<

5x4-symetrie/%.pdf: 5x4-symetrie/%.ipe
	ipetoipe -pdf $<

5x5-triangles/%.pdf: 5x5-triangles/%.ipe
	ipetoipe -pdf $<

5x8-aires/%.pdf: 5x8-aires/%.ipe
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

3ie:
	pdflatex 5x3-multiples/5x3-ie.tex
	pdflatex 5x3-multiples/5x3-ie.tex
	mv 5x3-ie.pdf '$(PDFDIR)'/5x3-ie.pdf

4ie:
	pdflatex 5x4-symetrie/5x4-ie.tex
	pdflatex 5x4-symetrie/5x4-ie.tex
	mv 5x4-ie.pdf '$(PDFDIR)'/5x4-ie.pdf	

5ie:
	pdflatex 5x5-triangles/5x5-ie.tex
	pdflatex 5x5-triangles/5x5-ie.tex
	mv 5x5-ie.pdf '$(PDFDIR)'/5x5-ie.pdf

6ie:
	pdflatex 5x6-proportionnalite/5x6-ie.tex
	pdflatex 5x6-proportionnalite/5x6-ie.tex
	mv 5x6-ie.pdf '$(PDFDIR)'/5x6-ie.pdf

7dm:
	pdflatex 5x7-statistiques/5x7-dm.tex
	pdflatex 5x7-statistiques/5x7-dm.tex
	mv 5x7-dm.pdf '$(PDFDIR)'/5x7-dm.pdf		

8ie:
	pdflatex 5x8-aires/5x8-ie.tex
	pdflatex 5x8-aires/5x8-ie.tex
	mv 5x8-ie.pdf '$(PDFDIR)'/5x8-ie.pdf

9ie:
	pdflatex 5x9-relatifs/5x9-ie.tex
	pdflatex 5x9-relatifs/5x9-ie.tex
	mv 5x9-ie.pdf '$(PDFDIR)'/5x9-ie.pdf

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
