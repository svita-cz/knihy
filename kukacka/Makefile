all:
	@echo "please use make <html>"

html:
	pandoc -o out/pro-kukacku.html --css style-html.css --toc --self-contained -s meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md

epub:
	pandoc -o out/pro-kukacku.epub -s meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md