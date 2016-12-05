CHAPTERS = meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md
all:
	@echo "please use make <html>"

html:
	pandoc -o out/pro-kukacku.html --css style-html.css --toc --self-contained -s $(CHAPTERS)

epub:
	pandoc -o out/pro-kukacku.epub -s $(CHAPTERS)

pdf:
	pandoc -o pro-kukacku.tex -t context --toc --self-contained --template=sablona.tex -s $(CHAPTERS)
	-rm pro-kukacku.pdf
	context pro-kukacku.tex
	mv pro-kukacku.pdf out/pro-kukacku.pdf

clean:
	rm out/*
