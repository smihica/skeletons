SCSS=scss
BUILDDIR=../../www
SRCS=$(shell ls **/*.scss)

.PHONY:		all clean

all:		init $(SRCS)
		$(SCSS) main.scss all.css
		mv all.css $(BUILDDIR)/all.css

rel:		init $(SRCS)
		$(SCSS) --style compressed main.scss all.css
		mv all.css $(BUILDDIR)/all.css

init:
		mkdir -p $(BUILDDIR)

clean:
		rm -f all.css $(BUILDDIR)/all.css
