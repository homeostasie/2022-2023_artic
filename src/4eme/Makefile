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
FIGSRC = $(wildcard 4x3-triangles-semblables/*.ipe 4x5-pythagore/*.ipe 4x8-pythagore-2/*.ipe 4xbb/*.ipe 4x10-trigonometrie/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x3-triangles-semblables/%.pdf: 4x3-triangles-semblables/%.ipe
	ipetoipe -pdf $<

4x5-pythagore/%.pdf: 4x5-pythagore/%.ipe
	ipetoipe -pdf $<

4x8-pythagore-2/%.pdf: 4x8-pythagore-2/%.ipe
	ipetoipe -pdf $<

4x10-trigonometrie/%.pdf: 4x10-trigonometrie/%.ipe
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

6ie:
	pdflatex 4x6-equations/4x6-ie.tex
	pdflatex 4x6-equations/4x6-ie.tex
	mv 4x6-ie.pdf '$(PDFDIR)'/4x6-ie-equations.pdf	

7murphy:
	pdflatex 4x7-probabilite/4x7-dm-murphy.tex
	pdflatex 4x7-probabilite/4x7-dm-murphy.tex
	mv 4x7-dm-murphy.pdf '$(PDFDIR)'/4x7-dm-murphy.pdf	

7rand:
	pdflatex 4x7-probabilite/4x7-dm-rand.tex
	pdflatex 4x7-probabilite/4x7-dm-rand.tex
	mv 4x7-dm-rand.pdf '$(PDFDIR)'/4x7-dm-rand.pdf	

7pb:
	pdflatex 4x7-probabilite/4x7-pb.tex
	pdflatex 4x7-probabilite/4x7-pb.tex
	mv 4x7-pb.pdf '$(PDFDIR)'/4x7-pb.pdf	


7ie:
	pdflatex 4x7-probabilite/4x7-ie.tex
	pdflatex 4x7-probabilite/4x7-ie.tex
	mv 4x7-ie.pdf '$(PDFDIR)'/4x7-ie.pdf

8dm:
	pdflatex 4x8-pythagore-2/4x8-dm.tex
	pdflatex 4x8-pythagore-2/4x8-dm.tex
	mv 4x8-dm.pdf '$(PDFDIR)'/4x8-dm-pythagore.pdf

9ie:
	pdflatex 4x9-equations-2/4x9-ie.tex
	pdflatex 4x9-equations-2/4x9-ie.tex
	mv 4x9-ie.pdf '$(PDFDIR)'/4x9-ie-equations-2.pdf	

10pb:
	pdflatex 4x10-trigonometrie/4x10-pb.tex
	pdflatex 4x10-trigonometrie/4x10-pb.tex
	mv 4x10-pb.pdf '$(PDFDIR)'/4x10-pb-trigo.pdf	

10gra:
	pdflatex 4x10-trigonometrie/4x10-graph.tex
	pdflatex 4x10-trigonometrie/4x10-graph.tex
	mv 4x10-graph.pdf '$(PDFDIR)'/4x10-graph-trigo.pdf	


10ie:
	pdflatex 4x10-trigonometrie/4x10-ie.tex
	pdflatex 4x10-trigonometrie/4x10-ie.tex
	mv 4x10-ie.pdf '$(PDFDIR)'/4x10-ie-trigo.pdf		

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
