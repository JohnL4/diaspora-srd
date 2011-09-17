# make rules: ensure that all chapter files are present

chapters: *.tex

# TODO: generate this TeX source from flat file
%.tex: $(LATEX_TXTDIR)/chapter/%/main.txt
	$(MAKE) -C $*
	touch $@


