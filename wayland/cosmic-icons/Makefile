COMMENT =	icons set for COSMIC desktop environment

V = 1.3.0

GH_ACCOUNT =	pop-os
GH_PROJECT =	cosmic-icons
GH_TAGNAME =	epoch-${V}

PKGNAME =	${GH_PROJECT}-${V}

CATEGORIES =	wayland

MAINTAINER =	Laurent Cheylus <foxy@free.fr>

# CC-BY-SA 4.0
PERMIT_PACKAGE=	Yes

RUN_DEPENDS =	x11/gtk+4,-guic

NO_BUILD =	Yes
NO_TEST =	Yes

ICONS_DIR = ${PREFIX}/share/icons/Cosmic

do-install:
	${INSTALL_DATA_DIR} ${ICONS_DIR}
	${INSTALL_DATA} ${WRKSRC}/index.theme ${ICONS_DIR}

	cd ${WRKSRC}/freedesktop && find ./scalable -type f -exec \
		install -Dm0644 {} ${ICONS_DIR}/{} \;
	cd ${WRKSRC}/extra && find ./scalable -type f -exec \
		install -Dm0644 {} ${ICONS_DIR}/{} \;

.include <bsd.port.mk>
