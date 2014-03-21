CATEGORY=	security/lectures
FILES=		intrusion.tex literature.tex infosak.bib
FILES+= 	dids.pdf honeypot.pdf profiles.pdf
#FILES+= 	agent.pdf bloomperf.pdf pwdhash.pdf
DOCUMENTS=	intrusion.pdf

PACKAGE=		intrusion-src
TARBALL_FILES=	${FILES} Makefile

PUB_FILES=	${DOCUMENTS} ${PACKAGE}.tar.gz

USE_LATEXMK= 	yes
USE_BIBLATEX= 	yes

intrusion.pdf: ${FILES}

#export no
TARBALL_FILES= 	${FILES} Makefile.export

Makefile.export: Makefile
infosak.bib: ../../infosak.bib
	${CP} $^ $@

clean:
	${RM} infosak.bib
#endexport

miun.depend.mk:
	wget http://ver.miun.se/build/$@

include miun.depend.mk
include miun.course.mk
include miun.package.mk
