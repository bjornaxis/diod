AM_CFLAGS = @WARNING_CFLAGS@

AM_CPPFLAGS = \
	-I$(top_srcdir)/libnpfs \
	-I$(top_srcdir)/liblsd \
	-I$(top_srcdir)/libdiod \
	$(LUA_INCLUDE)

sbin_PROGRAMS = diod

diod_LDADD = \
	$(top_builddir)/libdiod/libdiod.a \
	$(top_builddir)/libnpclient/libnpclient.a \
	$(top_builddir)/libnpfs/libnpfs.a \
	$(top_builddir)/liblsd/liblsd.a \
	$(LIBWRAP) $(LIBPTHREAD) $(LUA_LIB) $(LIBMUNGE) $(LIBCAP) \
	$(LIBIBVERBS) $(LIBRDMACM) $(LIBTCMALLOC)

diod_SOURCES = \
	diod.c \
	ops.c \
	ops.h \
	exp.c \
	exp.h \
	ioctx.c \
	ioctx.h \
	fid.c \
	fid.h \
	xattr.c \
	xattr.h

man8_MANS = \
        diod.8
