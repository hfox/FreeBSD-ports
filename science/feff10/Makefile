PORTNAME=	feff10
DISTVERSIONPREFIX=	v
DISTVERSION=	10.0.0-16
DISTVERSIONSUFFIX=	-gaa99129
CATEGORIES=	science

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Ab initio scattering calculations of X-ray absorption fine structure
WWW=		https://times-software.github.io/feff10/

LICENSE=	FEFF10
LICENSE_NAME=	FEFF10
LICENSE_FILE=	${WRKSRC}/../LICENSE
LICENSE_PERMS=	auto-accept dist-mirror pkg-mirror

BUILD_DEPENDS=	bash:shells/bash
RUN_DEPENDS=	bash:shells/bash

USES=		fortran gmake python:run shebangfix

USE_GITHUB=	yes
GH_ACCOUNT=	times-software

WRKSRC_SUBDIR=	src

SHEBANG_GLOB=	*.script

FFLAGS+=	-ffree-line-length-512 -fallow-argument-mismatch

MAKE_ARGS=	FLAGS="${FFLAGS}"

BINARY_ALIAS=	make=${GMAKE} ifort=${FC}

do-install:
	for f in ${WRKSRC}/../bin/Seq/*; do \
		if readelf -V $${f} > /dev/null 2>&1; then \
			${INSTALL_PROGRAM} $${f} ${STAGEDIR}${PREFIX}/bin; \
		else \
			${INSTALL_SCRIPT} $${f} ${STAGEDIR}${PREFIX}/bin; \
		fi \
	done

.include <bsd.port.mk>
