STATICS=$(shell ls *.html images/*)
BUILDDIR=build

dev:	init statics
	$(MAKE) -C scss
	$(MAKE) -C js

rel:	init statics
	$(MAKE) rel -C scss
	$(MAKE) rel -C js

statics: $(STATICS)
	cp -r *.html $(BUILDDIR)/
	cp -r images $(BUILDDIR)/

init:
	mkdir -p $(BUILDDIR)

clean:
	$(MAKE) clean -C scss
	$(MAKE) clean -C js
	rm -rf $(BUILDDIR)/*

.PHONY: dev clean