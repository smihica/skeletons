COMPRESS=uglifyjs
CONSTRUCT=../tools/jsconstruct
BUILDDIR=../build
SRCS=$(shell ls **/*.js)

.PHONY:		all clean

all:		all.js
		mv all.js $(BUILDDIR)/all.js

rel:		all.js
		$(COMPRESS) --unsafe -nc -o all.min.js all.js
		mv all.min.js $(BUILDDIR)/all.js
		rm all.js

all.js:		init $(SRCS)
		$(CONSTRUCT) -o all.js main.js

init:
		mkdir -p $(BUILDDIR)

clean:
		rm -f all.js all.min.js $(BUILDDIR)/all.js
