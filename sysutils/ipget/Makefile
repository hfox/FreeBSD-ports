PORTNAME=	ipget
DISTVERSIONPREFIX=	v
DISTVERSION=	0.9.1
PORTREVISION=	9
CATEGORIES=	sysutils

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Retrieve files over IPFS and save them locally
WWW=		https://github.com/ipfs/ipget

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:1.18,modules

GO_MODULE=	github.com/ipfs/ipget

PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
