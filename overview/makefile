all: pdf docx

pdf:
	pandoc --bibliography=../refs.bib --csl=../icesjms.csl manuscript.md -o manuscript.pdf

docx:
	pandoc --bibliography=../refs.bib --csl=../icesjms.csl manuscript.md -o manuscript.docx
