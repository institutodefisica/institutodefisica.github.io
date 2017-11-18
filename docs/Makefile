#all: guia.do.txt
all: | guia.md README.md guia.pdf
	$(guia.md)
	$(README.md)
	$(guia.pdf)

guia.md: guia.do.txt $(shell find partials -type f -regex ".*\.\do\.txt") 
	doconce format pandoc $^

guia.pdf: guia.md
	#pandoc $^ -o $@ --variable=fontfamily:arev --variable=geometry:margin=1in
	pandoc $^ -o $@ --variable=fontfamily:bera --variable=geometry:margin=1in

README.md: guia.do.txt
	$(guia.md)
	cp guia.md README.md
