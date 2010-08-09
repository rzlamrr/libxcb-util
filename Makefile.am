ACLOCAL_AMFLAGS = -I m4

MAINTAINERCLEANFILES = Makefile.in

SUBDIRS = atom aux event

AM_CFLAGS = $(CWARNFLAGS)

lib_LTLIBRARIES = libxcb-util.la

libxcb_util_la_CPPFLAGS = $(XCB_CFLAGS)
libxcb_util_la_LIBADD = $(XCB_LIBS)
libxcb_util_la_LDFLAGS = -version-info 0:0:0
libxcb_util_la_SOURCES = atom/atoms.c atom/atomlist.m4 atom/atoms.gperf.m4 \
	atom/xcb_atom.h.m4 event/event.c aux/xcb_aux.c

xcbinclude_HEADERS = xcb_util.h

pkgconfig_DATA = xcb-util.pc

EXTRA_DIST = xcb-util.pc.in
