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

### INCLUDES ###

INCLUDES= 	depend.mk miun.course.mk miun.package.mk export.mk

define inc
ifeq ($(findstring $(1),${MAKEFILE_LIST}),)
$(1):
	wget https://raw.githubusercontent.com/dbosk/makefiles/master/$(1)
include $(1)
endif
endef
$(foreach i,${INCLUDES},$(eval $(call inc,$i)))
