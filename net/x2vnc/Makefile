# $NetBSD: Makefile,v 1.24 2018/03/07 11:57:32 wiz Exp $

DISTNAME=		x2vnc-1.7.2
PKGREVISION=		3
CATEGORIES=		net x11
MASTER_SITES=		http://fredrik.hubbe.net/x2vnc/

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		http://fredrik.hubbe.net/x2vnc.html
COMMENT=		Multi-console display using X and VNC
LICENSE=		gnu-gpl-v2

GNU_CONFIGURE=		yes
LDFLAGS.SunOS+=		-lresolv -lsocket -lnsl

.include "options.mk"

.include "../../x11/libX11/buildlink3.mk"
.include "../../x11/libXScrnSaver/buildlink3.mk"
.include "../../x11/libXext/buildlink3.mk"
.include "../../x11/libXinerama/buildlink3.mk"
.include "../../x11/libXrandr/buildlink3.mk"
.include "../../x11/xorgproto/buildlink3.mk"

.include "../../mk/bsd.pkg.mk"
