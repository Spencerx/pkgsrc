# $NetBSD: Makefile,v 1.58 2018/07/04 13:40:19 jperkin Exp $
#

DISTNAME=	pioneers-0.11.3
PKGREVISION=	40
CATEGORIES=	games gnome
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=pio/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://pio.sourceforge.net/
COMMENT=	GNOME version of the Settlers of Catan board game

GNU_CONFIGURE=		YES
USE_TOOLS+=		gmake pkg-config msgfmt
USE_LIBTOOL=		YES
USE_PKGLOCALEDIR=	YES

BUILDLINK_DEPMETHOD.librsvg=	build	# generates icons

SUBST_CLASSES+=		paths
SUBST_STAGE.paths=	pre-configure
SUBST_MESSAGE.paths=	Fixing hardcoded paths.
SUBST_FILES.paths=	docs/*.6
SUBST_SED.paths=	-e s,/usr/share/,${PREFIX}/share/,

.include "../../devel/libgnome/buildlink3.mk"
.include "../../graphics/librsvg/buildlink3.mk"
.include "../../mk/omf-scrollkeeper.mk"
.include "../../x11/gtk2/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/bsd.pkg.mk"
