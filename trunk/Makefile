# Makefile for Diaspora SRD
#
# Our objective is to have an easy way to build any of the available 
# formats. So for instance, `make pdf` would compile the LaTeX 
# sources, while `make epub` would build an ePub file. We can also
# have more specific targets, so that we have `make pdf-landscape`
# for example.

pdf: diaspora-srd.pdf


epub: diaspora-srd.epub


.PHONY: clean
clean:
	rm tmpfiles

# LaTeX and PDF rules: we want to run make in the LaTeX subdirectory,
# then copy the resultant PDF to the current directory.
latexdir = latex
.PHONY: diaspora-srd.pdf
diaspora-srd.pdf: 
	$(MAKE) -C $(latexdir)
	cp $(latexdir)/diaspora-srd.pdf $@

# ePub rules: nothing yet; just put some dummy stuff here for now.
epubdir = epub
.PHONY: diaspora-srd.epub
diaspora-srd.epub: 
	$(MAKE) -C $(epubdir)
	cp $(epubdir)/diaspora-srd.epub $@

