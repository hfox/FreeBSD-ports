PORTNAME=	universal-ctags
PORTVERSION=	p6.0.20230319.0
CATEGORIES=	devel

MAINTAINER=	dereks@lifeofadishwasher.com
COMMENT=	Fork of Exuberant Ctags to generate index/tag files
WWW=		https://ctags.io/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		autoreconf gmake pkgconfig python:3.5+,test
USE_GITHUB=	yes
GH_PROJECT=	ctags

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--program-prefix=u

TEST_TARGET=	check

OPTIONS_DEFINE=		DEBUG ICONV JSON LIBXML2 MANPAGES PCRE2 YAML
OPTIONS_DEFAULT=	${OPTIONS_DEFINE:NDEBUG}
OPTIONS_SUB=		yes

JSON_DESC=	JSON output support
PCRE2_DESC=	${PCRE_DESC} v2

DEBUG_CONFIGURE_ENABLE=	debugging

ICONV_USES=		iconv
ICONV_CONFIGURE_ENABLE=	iconv

# Extra support for YAML and XML based languages
JSON_LIB_DEPENDS=	libjansson.so:devel/jansson
JSON_CONFIGURE_ENABLE=	json

LIBXML2_LIB_DEPENDS=		libxml2.so:textproc/libxml2
LIBXML2_CONFIGURE_ENABLE=	xml

MANPAGES_BUILD_DEPENDS=		rst2man:textproc/py-docutils
MANPAGES_CONFIGURE_WITH=	rst2man=${LOCALBASE}/bin/rst2man

PCRE2_LIB_DEPENDS=	libpcre2-8.so:devel/pcre2
PCRE2_CONFIGURE_ENABLE=	pcre2

YAML_LIB_DEPENDS=	libyaml.so:textproc/libyaml
YAML_CONFIGURE_ENABLE=	yaml

PORTSCOUT=	skipv:v6.0.0
.include <bsd.port.mk>
