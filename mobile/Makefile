XML2RFC=../../../xml2rfc/xml2rfc-1.35/xml2rfc.tcl

#DOCUMENT:=draft-kutscher-conex-mobile-03
DOCUMENT:=draft-ietf-conex-mobile-06
SOURCE:=draft-ietf-conex-mobile.xml
SOURCES:=$(SOURCE)

DRAFTTXT=$(DOCUMENT).txt


.PHONY: all
all: $(DOCUMENT).txt # $(DOCUMENT).pdf

#	tclsh $(XML2RFC) xml2rfc draft-conex-mobile.xml $(DRAFTTXT)


%.txt: $(SOURCES)
	sh $(XML2RFC) $(SOURCE) $@


%.ps: %.txt
	a2ps -1 --medium=Letter -L60 -l80 --borders=off -B -o $@ $<

%.pdf: %.ps
	ps2pdf $<




clean:
	rm -f $(DRAFTTXT) *~


