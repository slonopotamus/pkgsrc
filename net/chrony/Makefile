# $NetBSD: Makefile,v 1.44 2021/03/12 09:57:18 nia Exp $

DISTNAME=	chrony-4.0
CATEGORIES=	net
MASTER_SITES=	https://download.tuxfamily.org/chrony/

MAINTAINER=	hannken@NetBSD.org
HOMEPAGE=	https://chrony.tuxfamily.org/
COMMENT=	Daemon for maintaining the accuracy of computer clocks
LICENSE=	gnu-gpl-v2

USE_TOOLS+=		gmake
HAS_CONFIGURE=		YES
BUILD_DEFS+=		VARBASE
CONFIGURE_ARGS+=	--prefix=${PREFIX}
CONFIGURE_ARGS+=	--mandir=${PREFIX}/${PKGMANDIR}
CONFIGURE_ARGS+=	--sysconfdir=${PKG_SYSCONFDIR}
CONFIGURE_ARGS+=	--localstatedir=${VARBASE}
CONFIGURE_ARGS+=	--with-pidfile=${VARBASE}/run/chronyd.pid
AUTO_MKDIRS=		yes

OWN_DIRS=		${VARBASE}/lib/chrony

EGDIR=			${PREFIX}/share/examples/chrony
RCD_SCRIPTS=		chronyd

SUBST_CLASSES+=		paths
SUBST_FILES.paths=	examples/chrony.conf.example3
SUBST_VARS.paths=	PKG_SYSCONFDIR VARBASE
SUBST_STAGE.paths=	pre-configure

post-install:
	${INSTALL_DATA} "${WRKSRC}/examples/chrony.conf.example3" \
	    "${DESTDIR}${EGDIR}/chrony.conf.example";
	${INSTALL_DATA} "${WRKSRC}/examples/chrony.keys.example" \
	    "${DESTDIR}${EGDIR}/chrony.keys.example";

.include "options.mk"
.include "../../devel/editline/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
