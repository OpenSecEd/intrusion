.PHONY: all
all: notes.pdf slides.pdf

LATEXFLAGS+=	-shell-escape

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex

FIGS+= 		xkcd-341.png


notes.pdf: notes.tex
notes.pdf: ${SRC} $(addprefix figs/,${FIGS})

slides.pdf: slides.tex
slides.pdf: ${SRC} $(addprefix figs/,${FIGS})

$(addprefix figs/,${FIGS}):
	${MAKE} -C $(dir $@) $(notdir $@)


.PHONY: clean
clean:
	{RM} notes.pdf slides.pdf


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
