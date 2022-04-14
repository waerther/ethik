all: build/essay.pdf


build/essay.pdf: FORCE | build
	# to find header and bib files in the main directory
	TEXINPUTS=..: \
	BIBINPUTS=..: \
	max_print_line=1048576 \
	latexmk \
	  --lualatex \
	  --output-directory=build \
	  --interaction=nonstopmode \
	  --halt-on-error \
	essay.tex

build:
	mkdir -p build

clean:
	rm -rf build

FORCE:

.PHONY: all clean
