PANDOC = pandoc
FILES = $(wildcard *.md)

all: $(FILES:.md=.pdf) $(FILES:.md=.docx)
	@echo "informe copilado correctamente"

%.pdf: %.md
	$(PANDOC) $< -o $@ --pdf-engine=xelatex -V maintfoint="Liberation Sans" -V lang=ru

%.docx: %.md
	$(PANDOC) $< -o $@

clean:
	rm -f *.pdf *.docx
	@echo "archivos PDF y DOCX eliminados"

