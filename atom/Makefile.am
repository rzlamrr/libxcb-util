MAINTAINERCLEANFILES = Makefile.in

xcbinclude_HEADERS = xcb_atom.h

pkgconfig_DATA = xcb-atom.pc

EXTRA_DIST = xcb-atom.pc.in

BUILT_SOURCES = atoms.c atoms.gperf xcb_atom.h
CLEANFILES = $(BUILT_SOURCES)

atoms.c: atoms.gperf
	$(GPERF) --output-file $@ $<

atoms.gperf: atoms.gperf.m4 atomlist.m4
	$(M4) -I$(srcdir) $< >$@

xcb_atom.h: xcb_atom.h.m4 atomlist.m4
	$(M4) -I$(srcdir) $< >$@
