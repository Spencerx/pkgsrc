# $NetBSD: Makefile,v 1.3 2018/07/24 07:24:58 adam Exp $

DISTNAME=	pytest-testmon-0.9.13
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/py//}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=p/pytest-testmon/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/tarpas/pytest-testmon
COMMENT=	Py.test plug-in which selects tests affected by recent changes
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-coverage>=4.0.0:../../devel/py-coverage
DEPENDS+=	${PYPKGPREFIX}-test>=2.8.0:../../devel/py-test

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
