# $NetBSD: Makefile,v 1.3 2018/05/17 10:38:13 adam Exp $

DISTNAME=	confusable_homoglyphs-3.1.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	converters python
MASTER_SITES=	${MASTER_SITE_PYPI:=c/confusable_homoglyphs/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/vhf/confusable_homoglyphs
COMMENT=	Detect confusable usage of unicode homoglyphs
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-click-[0-9]*:../../devel/py-click

USE_LANGUAGES=	# none

post-install:
	cd ${DESTDIR}${PREFIX}/bin && ${MV} confusable_homoglyphs confusable_homoglyphs${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
