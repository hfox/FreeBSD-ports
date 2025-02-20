PORTNAME=	ghostscript
PORTVERSION=	7.07
PORTREVISION=	32
CATEGORIES=	print
MASTER_SITES=	SF/ghostscript/gnu-gs/${PORTVERSION}/
PKGNAMESUFFIX=	7-x11
DIST_SUBDIR=	${PORTNAME}

MAINTAINER=	hrs@FreeBSD.org
COMMENT=	Ghostscript 7.x PostScript interpreter, X11 support
WWW=		https://www.cs.wisc.edu/~ghost/doc/GPL/index.htm

LICENSE=	GPLv2

DEPRECATED=	Obsolete and unsupported upstream
EXPIRATION_DATE=2023-06-30

CONFLICTS_INSTALL= \
		gambc \
		ghostscript[789] \
		ghostscript[789]-nox11 \
		ghostscript9-agpl \
		ghostscript9-agpl-nox11

USES=		autoreconf cpe ghostscript:7 gmake tar:bzip2 xorg
USE_LDCONFIG=	yes
USE_XORG=	ice sm x11 xext xt
CPE_VENDOR=	artifex
GNU_CONFIGURE=	yes
CONFIGURE_ENV=	${MAKE_ENV}
CONFIGURE_ARGS=	--disable-compile-inits \
		--enable-dynamic \
		--without-ijs \
		--with-x \
		--x-includes=${LOCALBASE}/include \
		--x-libraries=${LOCALBASE}/lib
MAKE_ENV=	CFLAGS_STANDARD="${CFLAGS}" \
		XCFLAGS="${XCFLAGS}" XLDFLAGS="${XLDFLAGS}" \
		EXTRALIBS="${EXTRALIBS}"
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib
XLDFLAGS=	-lpthread
ALL_TARGET=	./obj/X11.so
INSTALL_TARGET=	install-shared
PLIST_FILES=	${GS_LIBDIR}/X11.so

GS_LIBDIR=	lib/${PORTNAME}/${PORTVERSION}

pre-build:
	${MKDIR} ${WRKSRC}/obj

.include <bsd.port.mk>
