all:
	@echo "please use make <html>"

html: amalgam
	pandoc -o zivot-v-mezerach.html --toc --self-contained -s zivot-v-mezerach.md

amalgam:
	cat 00-uvod.md 01-hry-s-ohnem.md 02-bludowsky-slavi-vanoce.md 03-sokoli-hnizdo.md 04-problem-tri-teles.md 05-osma-stopa.md 06-zazvor.md 07-zivot-v-mezerach.md 08-telepaticka.md 09-ohnova.md 10-marketa-slavi-vanoce.md 11-tiraz.md > zivot-v-mezerach.md

clean:
	rm zivot-v-mezerach.md
	rm zivot-v-mezerach.html