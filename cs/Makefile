export TEXINPUTS=../tex//:

all: prace.pdf

# LaTeX je potreba spustit nekolikrat, aby spravne spocital odkazy
prace.pdf: prace.tex $(wildcard *.tex) literatura.bib prace.xmpdata
	echo "================ First run ==============="
	pdflatex $<
	bibtex prace
	echo "================ Second run ==============="
	pdflatex $<
	echo "================ Third run ==============="
	pdflatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.xmpi
	rm -f prace.pdf
