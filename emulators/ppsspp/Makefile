PORTNAME=	ppsspp
DISTVERSIONPREFIX=	v
DISTVERSION?=	1.14.4
PORTREVISION?=	0
CATEGORIES=	emulators
# XXX Get from Debian once #697821 lands
MASTER_SITES=	https://bazaar.launchpad.net/~sergio-br2/${PORTNAME}/debian-sdl/download/5/${PORTNAME}.1-20140802045408-dd26dik367ztj5xg-8/:manpage
DISTFILES=	${PORTNAME}.1:manpage
EXTRACT_ONLY=	${DISTFILES:N*\:manpage:C/:.*//}

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	PSP emulator in C++ with dynarec JIT for x86, ARM, MIPS
WWW=		https://www.ppsspp.org/

LICENSE=	GPLv2+

# Bi-endian architectures default to big for some reason
NOT_FOR_ARCHS=	mips mips64 powerpc powerpc64 powerpcspe sparc64
NOT_FOR_ARCHS_REASON=	only little-endian is supported, see \
		https://github.com/hrydgard/ppsspp/issues/8823

LIB_DEPENDS=	libzip.so:archivers/libzip \
		libsnappy.so:archivers/snappy \
		libavcodec.so:multimedia/ffmpeg
RUN_DEPENDS=	xdg-open:devel/xdg-utils

USE_GITHUB=	yes
GH_ACCOUNT=	hrydgard
GH_TUPLE?=	hrydgard:glslang:8.13.3743-339-gdc11adde:glslang/ext/glslang \
		hrydgard:miniupnp:miniupnpd_2_1-502-g3a87be3:miniupnp/ext/miniupnp \
		facebook:zstd:v1.4.7-1276-g096dccbc:zstd/ext/zstd \
		unknownbrackets:ppsspp-debugger:9776332:debugger/assets/debugger \
		KhronosGroup:SPIRV-Cross:2021-01-15:SPIRV/ext/SPIRV-Cross \
		Kingcom:armips:v0.11.0-184-g6719ede:armips/ext/armips \
		Kingcom:filesystem:v1.3.2-12-g3f1c185:filesystem/ext/armips/ext/filesystem

CONFLICTS_INSTALL=	${PORTNAME}-*

USES=		cmake compiler:c++11-lib gl localbase:ldflags pkgconfig shared-mime-info
EXCLUDE=	libzip zlib
EXTRACT_AFTER_ARGS=${EXCLUDE:S,^,--exclude ,}
USE_GL=		glew opengl
CMAKE_ON=	USE_SYSTEM_FFMPEG USE_SYSTEM_LIBZIP USE_SYSTEM_SNAPPY USE_WAYLAND_WSI
CMAKE_OFF=	USE_DISCORD
SUB_FILES=	pkg-message
PORTDATA=	assets

DESKTOP_ENTRIES="PPSSPP" \
		"" \
		"${PORTNAME}" \
		"${PORTNAME} %f" \
		"Game;Emulator;" \
		""

OPTIONS_DEFINE=	VULKAN
OPTIONS_DEFAULT=VULKAN
OPTIONS_SINGLE=	GUI
OPTIONS_SINGLE_GUI=	LIBRETRO QT5 SDL
OPTIONS_SLAVE?=	SDL
OPTIONS_EXCLUDE:=	${OPTIONS_EXCLUDE} ${OPTIONS_SINGLE_GUI}

LIBRETRO_DESC=	libretro core for games/retroarch
LIBRETRO_CMAKE_BOOL=	LIBRETRO
LIBRETRO_PLIST_FILES=	lib/libretro/${PORTNAME}_libretro.so
LIBRETRO_VARS=	CONFLICTS_INSTALL= DESKTOP_ENTRIES= PLIST= PORTDATA= PKGMESSAGE= SUB_FILES=
QT5_USES=	qt:5 sdl
QT5_USE=	QT=qmake:build,buildtools:build,linguisttools:build,gui,multimedia,opengl,widgets
QT5_USE+=	SDL=sdl2 # audio, joystick
QT5_CMAKE_BOOL=	USING_QT_UI
QT5_VARS=	EXENAME=PPSSPPQt
SDL_CATEGORIES=		wayland
SDL_BUILD_DEPENDS=	png>=1.6:graphics/png
SDL_LIB_DEPENDS=	libpng.so:graphics/png
SDL_USES=	sdl
SDL_USE=	SDL=sdl2
SDL_VARS=	EXENAME=PPSSPPSDL
VULKAN_DESC=		Vulkan renderer
VULKAN_RUN_DEPENDS=	${LOCALBASE}/lib/libvulkan.so:graphics/vulkan-loader

post-patch:
	@${REINPLACE_CMD} -e 's/Linux/${OPSYS}/' \
		${WRKSRC}/assets/gamecontrollerdb.txt
	@${REINPLACE_CMD} -e 's,/usr/share,${PREFIX}/share,' \
		${WRKSRC}/UI/NativeApp.cpp
	@${REINPLACE_CMD} -e 's/"unknown"/"${DISTVERSIONFULL}"/' \
		${WRKSRC}/git-version.cmake

do-install-QT5-on do-install-SDL-on:
	${MV} ${STAGEDIR}${PREFIX}/bin/${EXENAME} \
		${STAGEDIR}${PREFIX}/bin/${PORTNAME}
	${INSTALL_MAN} ${_DISTDIR}/${PORTNAME}.1 \
		${STAGEDIR}${PREFIX}/share/man/man1

do-install-LIBRETRO-on:
	${MKDIR} ${STAGEDIR}${PREFIX}/${LIBRETRO_PLIST_FILES:H}
	${INSTALL_LIB} ${BUILD_WRKSRC}/lib/${LIBRETRO_PLIST_FILES:T} \
		${STAGEDIR}${PREFIX}/${LIBRETRO_PLIST_FILES:H}

.include <bsd.port.mk>
