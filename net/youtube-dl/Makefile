# $NetBSD: Makefile,v 1.141 2018/07/22 10:16:11 leot Exp $

# XXX: VERSION_DATE can contains also an optional part that indicates
# XXX: possible same day revisions. PKGNAME preserves that dotted part as is.
VERSION_DATE=	2018.07.21
DISTNAME=	youtube-dl-${VERSION_DATE}
PKGNAME=	${DISTNAME:S/.//:S/.//}
CATEGORIES=	net
MASTER_SITES=	http://youtube-dl.org/downloads/${VERSION_DATE}/

MAINTAINER=	leot@NetBSD.org
HOMEPAGE=	http://rg3.github.io/youtube-dl/
COMMENT=	Download videos from youtube.com
LICENSE=	public-domain

USE_LANGUAGES=	# none
EGG_NAME=	youtube_dl-${VERSION_DATE:S/.0/./g}
WRKSRC=		${WRKDIR}/youtube-dl

SUBST_CLASSES+=		pkgmandir
SUBST_STAGE.pkgmandir=	pre-configure
SUBST_FILES.pkgmandir=	setup.py
SUBST_VARS.pkgmandir=	PKGMANDIR

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
