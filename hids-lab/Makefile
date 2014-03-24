DOCUMENTS= 	hids.pdf
FILES= 		hids.tex aims.tex literature.tex literature.bib
CATEGORY= 	security/labs

PACKAGE= 		hids-src
TARBALL_FILES= 	${FILES} Makefile

PUB_FILES= 		${PACKAGE}.tar.gz ${DOCUMENTS}

USE_LATEXMK= 	yes
USE_BIBLATEX= 	yes

hids.pdf: ${FILES}

clean:
	${RM} ${DOCUMENTS}

#export no
literature.bib: ../../infosak.bib
	${CP} $^ $@

clean:
	${RM} literature.bib ${DOCUMENTS}

TARBALL_FILES= 	${FILES:.tex=.exporttex} Makefile.export

Makefile.export: Makefile
#endexport

miun.depend.mk:
	wget http://ver.miun.se/build/$@

include miun.depend.mk
include miun.course.mk
include miun.package.mk
