dnl XCB_UTIL_M4_WITH_INCLUDE_PATH requires Autoconf >= 2.62
AC_PREREQ(2.62)
AC_INIT([xcb-util-core],0.3.7,[xcb@lists.freedesktop.org])
AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([foreign dist-bzip2])
AM_MAINTAINER_MODE

XCB_UTIL_M4_WITH_INCLUDE_PATH
XCB_UTIL_COMMON([1.4], [1.6])

AC_CHECK_PROGS(GPERF, gperf, [no])
if test $GPERF = "no"; then
        AC_MSG_ERROR([Can't find gperf, please install it and try again])
fi

AC_CHECK_FUNCS_ONCE(vasprintf)
AC_TYPE_SSIZE_T

PKG_CHECK_MODULES(XPROTO, xproto >= 7.0.8)

AC_OUTPUT([Makefile xcb-util.pc
	aux/Makefile aux/xcb-aux.pc
	atom/Makefile atom/xcb-atom.pc
	event/Makefile event/xcb-event.pc
	xcb_util_intro
	])
