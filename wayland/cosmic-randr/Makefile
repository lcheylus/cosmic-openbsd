COMMENT =	tools for displaying and configuring Wayland outputs

V = 1.3.0

GH_ACCOUNT =	pop-os
GH_PROJECT =	cosmic-randr
GH_TAGNAME =	epoch-${V}

PKGNAME =	${GH_PROJECT}-${V}

CATEGORIES =	wayland

MAINTAINER =	Laurent Cheylus <foxy@free.fr>

# MPL-2.0
PERMIT_PACKAGE=	Yes

WANTLIB +=	${MODCARGO_WANTLIB}

MODCARGO_CRATES += cosmic-protocols 0.2.0  # GPL-3.0

MODULES =	devel/cargo

CONFIGURE_STYLE=	cargo
SEPARATE_BUILD =	Yes

do-install:
	${INSTALL_PROGRAM} ${MODCARGO_TARGET_DIR}/release/cosmic-randr ${PREFIX}/bin/

.include "crates.inc"

.include <bsd.port.mk>
