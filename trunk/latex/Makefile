# make rules for LaTeX-generated PDF version of the SRD.

# The command to run LaTeX:
LATEX = pdflatex
export LATEX_TXTDIR := $(abspath ../text)

pdf: diaspora-srd.pdf

diaspora-pdf: diaspora-srd.tex
	$(LATEX) $<

diaspora-srd.tex: \
		$(chapters) \
		$(sidebars) \
		$(tables) \
		$(db) \
		$(appendices) \
		$(includes)

### The various parts of the LaTeX file tree: ###
chapters = chapter/*.tex 
chapter/%.tex: chapter/%/*.tex
	touch $@
# to do later: generate these TeX files from flat text files
chapter/%.tex: 

db:
	$(MAKE) -C db


