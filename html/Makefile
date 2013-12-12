STATICS=$(shell ls *.html images/*)
BUILDDIR=www

dev:
	$(MAKE) -C src

rel:
	$(MAKE) rel -C src

auto:	dev
	./tools/update-watcher src/*.html src/scss/*.scss src/scss/**/*.scss src/js/*.js src/js/**/*.js -- $(MAKE) -C src

clean:
	$(MAKE) clean -C src

.PHONY: dev clean
