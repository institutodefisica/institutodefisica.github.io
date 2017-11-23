#all: guia.do.txt
all: | index.html guia.md README.md guia.pdf
	$(guia.md)
	$(README.md)
	$(guia.pdf)

index.html: guia.do.txt
	$(guia.md)
	doconce format html $^
	mv -f guia.html index.html

guia.md: guia.do.txt $(shell find partials -type f -regex ".*\.\do\.txt") 
	doconce format pandoc $^

guia.pdf: guia.md
	#pandoc $^ -o $@ --variable=fontfamily:arev --variable=geometry:margin=1in
	pandoc $^ -o $@ --variable=fontfamily:bera --variable=geometry:margin=1in

README.md: guia.do.txt
	$(guia.md)
	cp -f guia.md README.md
