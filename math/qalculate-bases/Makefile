# $NetBSD: Makefile,v 1.45 2018/04/16 14:34:52 wiz Exp $

DISTNAME=	qalculate-bases-0.9.4
PKGREVISION=	30
CATEGORIES=	math
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=qalculate/}

MAINTAINER=	adam@NetBSD.org
HOMEPAGE=	http://qalculate.sourceforge.net/
COMMENT=	Utility for conversion between number bases using Qalculate

USE_LANGUAGES=		c c++
USE_LIBTOOL=		yes
USE_PKGLOCALEDIR=	yes
USE_TOOLS+=		autoconf gmake intltool msgfmt pkg-config
GNU_CONFIGURE=		yes

pre-configure:
	${RUN} cd ${WRKSRC}; autoconf

.include "../../math/qalculate/buildlink3.mk"
.include "../../x11/gtk2/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/bsd.pkg.mk"
