# $NetBSD: Makefile,v 1.1 2021/04/07 16:14:08 tnn Exp $

PKGNAME=	gnuradio-network-${VERSION}
COMMENT=	Network blocks for GNU Radio

.include	"../../ham/gnuradio-core/Makefile.common"
.include	"../../ham/gnuradio-core/Nocore.mk"

CMAKE_ARGS+=	-DENABLE_DEFAULT=OFF
CMAKE_ARGS+=	-DENABLE_GR_NETWORK=ON
CMAKE_ARGS+=	-DENABLE_GRC=ON

PLIST_MINUS+=	companion

.include	"../../mk/bsd.pkg.mk"
