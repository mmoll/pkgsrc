# $NetBSD: Makefile,v 1.47 2018/07/20 03:34:03 ryoon Exp $

DISTNAME=	qsynth-0.4.1
PKGREVISION=	16
CATEGORIES=	audio
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=qsynth/}
EXTRACT_USING=	bsdtar

MAINTAINER=	adam@NetBSD.org
HOMEPAGE=	http://qsynth.sourceforge.net/
COMMENT=	Qt GUI Interface to FluidSynth
LICENSE=	gnu-gpl-v2

USE_LANGUAGES=		c c++
USE_LIBTOOL=		yes
USE_TOOLS+=		gmake
GNU_CONFIGURE=		yes

PTHREAD_AUTO_VARS=	yes

.include "options.mk"

.include "../../audio/fluidsynth/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
