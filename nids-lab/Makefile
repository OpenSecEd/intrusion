DOCUMENTS= 	nids.pdf
FILES= 		nids.tex aims.tex literature.tex literature.bib
CATEGORY= 	security/labs

PACKAGE= 		nids-src
TARBALL_FILES= 	${FILES} Makefile

PUB_FILES= 		${PACKAGE}.tar.gz ${DOCUMENTS}

nids.pdf: ${FILES}

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
