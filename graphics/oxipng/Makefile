PORTNAME=	oxipng
DISTVERSION=	8.0.0
PORTREVISION=	3
CATEGORIES=	graphics
MASTER_SITES=	CRATESIO
# XXX Teach USES=cargo to have proper default
DISTFILES=	${CARGO_DIST_SUBDIR}/${DISTNAME}${CARGO_CRATE_EXT}

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	Multithreaded PNG optimizer written in Rust
WWW=		https://github.com/shssoichiro/oxipng

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		cargo
PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
