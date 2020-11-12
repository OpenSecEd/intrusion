.PHONY: all
all: notes.pdf slides.pdf

LATEXFLAGS+=	-shell-escape

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex

FIGS+= 		xkcd-341.png
FIGS+= 		skatteverket-hack.png
FIGS+=		behaviour-profiles.pdf
FIGS+=		network-rotated.pdf
FIGS+=		network-layers.pdf
FIGS+=		ruag-turla.png
FIGS+=		nsa-leak.png snowden.png


notes.pdf: notes.tex
notes.pdf: ${SRC} $(addprefix figs/,${FIGS})

slides.pdf: slides.tex
slides.pdf: ${SRC} $(addprefix figs/,${FIGS})

$(addprefix figs/,${FIGS})::
	${MAKE} -C $(dir $@) $(notdir $@)


.PHONY: clean
clean:
	${RM} notes.pdf slides.pdf


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
