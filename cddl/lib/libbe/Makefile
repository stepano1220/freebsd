# $FreeBSD$

PACKAGE=	lib${LIB}
LIB=		be
SHLIB_MAJOR=	1
SHLIB_MINOR=	0
LIBBE_SRC=	${SRCTOP}/lib/libbe

.PATH:	${LIBBE_SRC}
SRCS=		be.c be_access.c be_error.c be_info.c
INCS=		be.h
MAN=		libbe.3

WARNS?=	2

LIBADD+= zfs
LIBADD+= nvpair

CFLAGS+= -I${LIBBE_SRC}
CFLAGS+= -I${SRCTOP}/cddl/contrib/opensolaris/lib/libzfs/common
CFLAGS+= -I${SRCTOP}/sys/cddl/compat/opensolaris
CFLAGS+= -I${SRCTOP}/cddl/compat/opensolaris/include
CFLAGS+= -I${SRCTOP}/cddl/compat/opensolaris/lib/libumem
CFLAGS+= -I${SRCTOP}/cddl/contrib/opensolaris/lib/libzpool/common
CFLAGS+= -I${SRCTOP}/sys/cddl/contrib/opensolaris/common/zfs
CFLAGS+= -I${SRCTOP}/sys/cddl/contrib/opensolaris/uts/common/fs/zfs
CFLAGS+= -I${SRCTOP}/sys/cddl/contrib/opensolaris/uts/common
CFLAGS+= -I${SRCTOP}/cddl/contrib/opensolaris/head
LDFLAGS+= -v

CFLAGS+= -DNEED_SOLARIS_BOOLEAN

.include <bsd.lib.mk>
