# $NetBSD: Makefile,v 1.10 2018/07/18 00:06:10 joerg Exp $
#

DISTNAME=	milkytracker-0.90.86
PKGREVISION=	1
CATEGORIES=	audio
MASTER_SITES=	http://milkytracker.org/files/
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	jkuittinen@users.sourceforge.net
HOMEPAGE=	http://milkytracker.org/
COMMENT=	Music tracker inspired by Fast Tracker 2
LICENSE=	gnu-gpl-v3

GNU_CONFIGURE=	yes
USE_LANGUAGES=	c c++03
USE_TOOLS+=	gawk

.include "options.mk"

INSTALLATION_DIRS+=	share/doc/milkytracker
INSTALLATION_DIRS+=	share/examples/milkytracker

DOCDIR=			${DESTDIR}${PREFIX}/share/doc/milkytracker

post-install:
	${INSTALL_DATA} ${WRKSRC}/docs/* ${DOCDIR}

.include "../../converters/libiconv/buildlink3.mk"
.include "../../devel/SDL/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
