all:
	@echo "please use make <html>"

html:
	pandoc -o out/pro-kukacku.html --css style-html.css --toc --self-contained -s meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md

epub:
	pandoc -o out/pro-kukacku.epub -s meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md

pdf:
	pandoc -o pro-kukacku.tex -t context --toc --self-contained --template=sablona.tex -s meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md
	-rm pro-kukacku.pdf
	context pro-kukacku.tex
	mv pro-kukacku.pdf out/pro-kukacku.pdf

clean:
	rm out/*