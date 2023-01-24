# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/bb
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)


bb:
	latex bb-2023.tex
	dvips bb-2023.dvi
	ps2pdf bb-2023.ps
	mv bb-2023.pdf '$(PDFDIR)'/bb-2023.pdf

ex1:
	latex ex1.tex
	dvips ex1.dvi
	ps2pdf ex1.ps

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
