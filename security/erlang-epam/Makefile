# $NetBSD: Makefile,v 1.4 2018/03/24 14:29:19 fhajny Exp $

DISTNAME=	epam-1.0.4
CATEGORIES=	security
MASTER_SITES=	${MASTER_SITE_GITHUB:=processone/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/processone/epam/
COMMENT=	epam helper for Erlang / Elixir PAM authentication support
LICENSE=	gnu-gpl-v2

GITHUB_PROJECT=	epam

SUPERSEDES=	erlang-p1_epam-[0-9]*

GNU_CONFIGURE=	yes

LDFLAGS.SunOS+=	-lnsl

.include "../../lang/erlang/module.mk"
.include "../../mk/bsd.pkg.mk"
