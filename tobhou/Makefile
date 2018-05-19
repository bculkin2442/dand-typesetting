.PHONY: all clean preview

%.ms: $(wildcard ../macros/*.tmac)

%.ps: %.ms
	groff -Tps -ms $< > $@

%.pdf: %.ps
	pstopdf $< -o $@

tobhou.ms: races.ms
	touch tobhou.ms

all: tobhou.pdf

preview: tobhou.pdf
	open tobhou.pdf

clean:
	rm -f tobhou.pdf
