# $NetBSD: Makefile,v 1.25 2021/04/01 18:45:33 wiz Exp $
#
# Release notes:
# https://github.com/golang/tools/releases

DISTNAME=	gopls-0.6.9
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=golang/}
GITHUB_PROJECT=	tools
GITHUB_TAG=	gopls/v${PKGVERSION_NOREV}

MAINTAINER=	bsiegert@NetBSD.org
HOMEPAGE=	https://pkg.go.dev/golang.org/x/tools/gopls
COMMENT=	LSP server for Go editor integration
LICENSE=	modified-bsd

WRKSRC=		${WRKDIR}/tools-${GITHUB_TAG:S/\//-/}/gopls

GO_BUILD_PATTERN=	.

CHECK_RELRO_SKIP+=	bin/gopls

.include "go-modules.mk"

.include "../../lang/go/go-module.mk"
.include "../../mk/bsd.pkg.mk"
