dnl Process this file with autoconf to produce a configure script.
AC_INIT(robotfindskitten, [2.8284271.702], [rfk-dev@sourceforge.net], robotfindskitten)
AM_INIT_AUTOMAKE([gnu])
dnl Make builds less verbose.  Shuts off Makefile portability checks.
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_CONFIG_MACRO_DIRS([m4])
AM_CONFIG_HEADER(config.h)
AC_LANG_C

dnl Checks for programs.
AC_PROG_CC
AM_PROG_LIBTOOL
AC_PROG_INSTALL

dnl Checks for libraries.
AC_CHECK_LIB(ncurses, initscr, ,curses)

dnl Checks for header files.
AC_CHECK_HEADERS(signal.h)
AC_CHECK_HEADERS(ncurses.h,, 
	[AC_CHECK_HEADERS(curses.h,, 
		AC_MSG_ERROR(Could not find ncurses headers!))])

# This will become the directory name on SourceForge
TAGLINE='ship_it_anyway'
AC_SUBST(TAGLINE)

AC_OUTPUT(Makefile src/Makefile doc/Makefile nki/Makefile share/Makefile)
