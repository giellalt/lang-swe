# A makefile to help conversion from the SALDO format to LexC.

all: paradigms

swe-words-paradigms.txt: saldo_2.3/saldo20v03.txt
	grep -v '^#' $< | cut -f5,7 > $@

paradigms: swe-words-paradigms.txt
	./scrape-saldo-paradigms.sh

clean:
	-rm -f swe-words-paradigms.txt
	-rm -rf paradigms
