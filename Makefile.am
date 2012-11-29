
AM_CFLAGS = @THREADSAFE_FLAGS@ @DYNAMIC_EXTENSION_FLAGS@ -DSQLITE_ENABLE_FTS3 -DSQLITE_ENABLE_RTREE

lib_LTLIBRARIES = libsqlite3_vbts.la
libsqlite3_vbts_la_SOURCES = sqlite3.c
libsqlite3_vbts_la_LDFLAGS = -no-undefined -version-info 8:6:8

bin_PROGRAMS = sqlite3_vbts
sqlite3_vbts_SOURCES = shell.c sqlite3.h
sqlite3_vbts_LDADD = $(top_builddir)/libsqlite3_vbts.la @READLINE_LIBS@
sqlite3_vbts_DEPENDENCIES = $(top_builddir)/libsqlite3_vbts.la

include_HEADERS = sqlite3.h sqlite3ext.h

EXTRA_DIST = sqlite3.pc sqlite3.1 tea
pkgconfigdir = ${libdir}/pkgconfig
pkgconfig_DATA = sqlite3.pc

man_MANS = sqlite3.1
