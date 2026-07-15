COMMENT =	wallpapers for the COSMIC Desktop Environment

V = 1.3.0

GH_ACCOUNT =	pop-os
GH_PROJECT =	cosmic-wallpapers
GH_TAGNAME =	epoch-${V}

PKGNAME =	${GH_PROJECT}-${V}

CATEGORIES =	wayland

MAINTAINER =	Laurent Cheylus <foxy@free.fr>

# CC-BY-SA 4.0
PERMIT_PACKAGE=	Yes

NO_BUILD =	Yes
NO_TEST =	Yes

DATA_DIR = ${PREFIX}/share/backgrounds/cosmic

do-install:
	${INSTALL_DATA_DIR} ${DATA_DIR}
	cd ${WRKSRC}/original && pax -rw . ${DATA_DIR}

.include <bsd.port.mk>
