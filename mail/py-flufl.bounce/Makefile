# $NetBSD: Makefile,v 1.2 2018/07/03 05:03:23 adam Exp $

DISTNAME=	flufl.bounce-3.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	mail
MASTER_SITES=	${MASTER_SITE_PYPI:=f/flufl.bounce/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://launchpad.net/flufl.bounce/
COMMENT=	Email bounce detectors
LICENSE=	apache-2.0

PYTHON_VERSIONS_ACCEPTED=	37 36 35 34

DEPENDS+=	${PYPKGPREFIX}-atpublic-[0-9]*:../../devel/py-atpublic
DEPENDS+=	${PYPKGPREFIX}-ZopeInterface-[0-9]*:../../devel/py-ZopeInterface

BUILD_DEPENDS+=	${PYPKGPREFIX}-nose2-[0-9]*:../../devel/py-nose2

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
