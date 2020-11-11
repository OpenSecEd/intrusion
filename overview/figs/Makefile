xkcd-341.png:
	curl -o $@ https://imgs.xkcd.com/comics/1337_part_1.png 

behaviour-profiles.pdf: behaviour-profiles.svg

%-crop.pdf: %.pdf
	pdfcrop $<

network.pdf: network.svg
network-rotated.pdf: network.pdf
	pdftk $< cat 1-endeast output $@

network-layers.pdf: network-layers.svg


.PHONY: clean
clean:
	${RM} xkcd-341.png
	${RM} behaviour-profiles.pdf behaviour-profiles.pdf_tex
	${RM} *-crop.pdf
	${RM} network.pdf network.pdf_tex network-rotated.pdf
	${RM} network-layers.pdf network-layers.pdf_tex


INCLUDE_MAKEFILES?=../../makefiles
include ${INCLUDE_MAKEFILES}/doc.mk
