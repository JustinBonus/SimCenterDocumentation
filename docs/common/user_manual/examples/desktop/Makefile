
.PHONY : ee we rdt pbe qfem pelicun hydro

SIMCENTER_DEV = ../../../../../..
SRCDIR = $(SIMCENTER_DEV)/$(SIMDOC_APP)/examples
RENDRE = rendre -D $(SRCDIR)/.aurore/aurore.cache.json


ee:      SIMDOC_APP=EE-UQ
we:      SIMDOC_APP=WE-UQ
rdt:     SIMDOC_APP=RDT
pbe:     SIMDOC_APP=PBE
qfem:    SIMDOC_APP=quoFEM
pelicun: SIMDOC_APP=pelicun
hydro:   SIMDOC_APP=HydroUQ
export   SIMDOC_APP

TARGETS = $(shell $(RENDRE) list --line -- \%./doc)
SOURCES = $(addprefix $(SRCDIR)/./,$(TARGETS))

ee we rdt pbe qfem pelicun hydro:
	rsync -Rcv $(SOURCES) .


