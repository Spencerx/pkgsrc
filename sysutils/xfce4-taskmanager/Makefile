# $NetBSD: Makefile,v 1.12 2018/08/22 09:46:43 wiz Exp $

PKGREVISION= 4
.include "../../meta-pkgs/xfce4/Makefile.common"

DISTNAME=	xfce4-taskmanager-1.2.0
CATEGORIES=	sysutils
MASTER_SITES=	http://archive.xfce.org/src/apps/xfce4-taskmanager/1.2/

HOMEPAGE=	http://goodies.xfce.org/projects/applications/xfce4-taskmanager
COMMENT=	Xfce task manager

# patch needs libkvm.
.include "../../mk/bsd.prefs.mk"
.if ${OPSYS} != "Linux"
LDFLAGS+=	-lkvm
.endif

.include "../../x11/gtk2/buildlink3.mk"
.include "../../x11/libXmu/buildlink3.mk"
.include "../../x11/libxfce4ui/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
