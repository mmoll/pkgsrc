# $NetBSD: Makefile,v 1.40 2018/07/20 03:33:55 ryoon Exp $
#

DISTNAME=	softhsm-1.3.7
PKGREVISION=	12
CATEGORIES=	security
MASTER_SITES=	https://www.opendnssec.org/files/source/

MAINTAINER=	pettai@NetBSD.org
HOMEPAGE=	https://www.opendnssec.org/softhsm/
COMMENT=	Cryptographic store accessible through a PKCS\#11 interface
LICENSE=	2-clause-bsd

BUILD_DEFS+=	VARBASE

USE_LANGUAGES=	c c++
USE_LIBTOOL=	yes

GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--localstatedir=${VARBASE}
CONFIGURE_ARGS+=	--with-botan=${PREFIX}

EGDIR=			${PREFIX}/share/examples/softhsm

SUBST_CLASSES+=         paths
SUBST_FILES.paths=      ${WRKSRC}/Makefile.in
SUBST_STAGE.paths=      pre-configure
SUBST_SED.paths=        -e 's,@EGDIR@,${EGDIR},'

CXXFLAGS.NetBSD+=	-D_NETBSD_SOURCE

CONF_FILES=		${EGDIR}/softhsm.conf ${PKG_SYSCONFDIR}/softhsm.conf

INSTALLATION_DIRS=	${EGDIR} etc bin lib
OWN_DIRS=		${VARBASE}/softhsm

pre-install:
	${INSTALL_DATA} ${WRKSRC}/softhsm.conf ${DESTDIR}${EGDIR}

.include "../../databases/sqlite3/buildlink3.mk"
.include "../../security/botan/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
