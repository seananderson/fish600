all: pdf docx

pdf:
	pandoc --template=reference.tex --bibliography=refs.bib --csl=icesjms.csl manuscript.md -o manuscript.pdf

docx:
	pandoc --reference-docx=reference.docx --bibliography=refs.bib --csl=icesjms.csl manuscript.md -o manuscript.docx
