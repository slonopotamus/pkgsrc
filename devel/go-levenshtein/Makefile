# $NetBSD: Makefile,v 1.10 2021/03/19 17:36:58 bsiegert Exp $

DISTNAME=	go-levenshtein-1.2.3
MASTER_SITES=	${MASTER_SITE_GITHUB:=agext/}
PKGREVISION=	9
CATEGORIES=	devel
GITHUB_PROJECT=	levenshtein
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/agext/levenshtein
COMMENT=	Levenshtein distance and similarity metrics
LICENSE=	apache-2.0

GO_DIST_BASE=	${DISTNAME:S,go-,,}
GO_SRCPATH=	github.com/agext/levenshtein

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
