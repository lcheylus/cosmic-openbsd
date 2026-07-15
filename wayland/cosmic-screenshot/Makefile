COMMENT =	COSMIC tool to capture screenshot

V = 1.3.0

GH_ACCOUNT =	pop-os
GH_PROJECT =	cosmic-screenshot
GH_TAGNAME =	epoch-${V}

PKGNAME =	${GH_PROJECT}-${V}

CATEGORIES =	wayland

MAINTAINER =	Laurent Cheylus <foxy@free.fr>

# MPL-2.0
PERMIT_PACKAGE=	Yes

WANTLIB +=	${MODCARGO_WANTLIB} m

RUN_DEPENDS =	devel/desktop-file-utils \
		x11/gtk+4,-guic

MODULES =	devel/cargo

CONFIGURE_STYLE=	cargo
SEPARATE_BUILD =	Yes

# No tests implemented in Rust sources
NO_TEST =	Yes

SIZES =	16x16 24x24 32x32 48x48 64x64 128x128 256x256

do-install:
	${INSTALL_PROGRAM} ${MODCARGO_TARGET_DIR}/release/cosmic-screenshot ${PREFIX}/bin/

	${INSTALL_DATA_DIR} ${PREFIX}/share/applications/
	${INSTALL_DATA} ${WRKSRC}/resources/com.system76.CosmicScreenshot.desktop \
		${PREFIX}/share/applications/

	${INSTALL_DATA_DIR} ${PREFIX}/share/icons/hicolor/

.for size in ${SIZES}
	${INSTALL_DATA_DIR} ${PREFIX}/share/icons/hicolor/${size}/apps/
	${INSTALL_DATA} ${WRKSRC}/resources/icons/hicolor/${size}/apps/com.system76.CosmicScreenshot.svg \
		${PREFIX}/share/icons/hicolor/${size}/apps/
.endfor

.include "crates.inc"

.include <bsd.port.mk>
