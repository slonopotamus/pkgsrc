# $NetBSD: Makefile,v 1.15 2021/03/30 10:58:26 markd Exp $

DISTNAME=	kdav-${KF5VER}
CATEGORIES=	misc

HOMEPAGE=	https://community.kde.org/Frameworks
COMMENT=	DAV protocol implemention with KJobs
LICENSE=	gnu-lgpl-v2

.include "../../meta-pkgs/kde/kf5.mk"

USE_TOOLS+=	msgmerge

.include "../../devel/kio/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
