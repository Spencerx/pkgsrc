# $NetBSD: Makefile,v 1.10 2018/07/03 05:03:43 adam Exp $

PKGREVISION= 5
.include "../../x11/keybinder/Makefile.common"

PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	x11 python

MAINTAINER=	pkgsrc-users@NetBSD.org
COMMENT=	Python bindings for the keybinder library
LICENSE=	gnu-gpl-v2

CONFIGURE_ARGS+=	--disable-lua
CONFIGURE_ARGS+=	--enable-python

PY_PATCHPLIST=			yes
PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36 37

INSTALL_DIRS=	python-keybinder

.include "../../lang/python/extension.mk"
.include "../../x11/py-gtk2/buildlink3.mk"
.include "../../x11/keybinder/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
