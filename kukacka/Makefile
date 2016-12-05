CHAPTERS = meta.md pro-kukacku.md hrdlicka.md pod-vlivem.md tiraz.md

.PHONY: all clean
.PRECIOUS: out/%.html out/%.epub out/%.pdf

all: html epub pdf

clean:
	rm out/*

%: out/pro-kukacku.% ;

out/%.html: | $(CHAPTERS) style-html.css $(MAKEFILE_LIST)
	pandoc -o $@ --css style-html.css --toc --self-contained -s $(CHAPTERS)

out/%.epub: | $(CHAPTERS) $(MAKEFILE_LIST)
	pandoc -o $@ -s $(CHAPTERS)

out/%.pdf: %.tex | $(MAKEFILE_LIST)
	context $< --batch-mode --purgeresult --result=$@

%.tex: | $(CHAPTERS) sablona.contex $(MAKEFILE_LIST)
	pandoc -o $@ -t context --toc --self-contained --template=sablona.contex -s $(CHAPTERS)
