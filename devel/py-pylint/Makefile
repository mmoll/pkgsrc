# $NetBSD: Makefile,v 1.29 2018/08/02 15:19:23 adam Exp $

DISTNAME=	pylint-2.1.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=p/pylint/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://www.pylint.org/
COMMENT=	Python source code analyzer
LICENSE=	gnu-gpl-v2

DEPENDS+=	${PYPKGPREFIX}-astroid>=2.0.1:../../devel/py-astroid
DEPENDS+=	${PYPKGPREFIX}-isort>=4.2.5:../../devel/py-isort
DEPENDS+=	${PYPKGPREFIX}-mccabe-[0-9]*:../../devel/py-mccabe
BUILD_DEPENDS+=	${PYPKGPREFIX}-test-runner-[0-9]*:../../devel/py-test-runner
TEST_DEPENDS+=	${PYPKGPREFIX}-test-[0-9]*:../../devel/py-test

USE_LANGUAGES=	# none

PYTHON_VERSIONS_INCOMPATIBLE=	27

INSTALLATION_DIRS=	${PKGMANDIR}/man1

REPLACE_PYTHON+=	pylint/test/data/ascript

post-install:
.for file in epylint pylint pyreverse symilar
	${MV} ${DESTDIR}${PREFIX}/bin/${file} ${DESTDIR}${PREFIX}/bin/${file}${PYVERSSUFFIX} || ${TRUE}
	${INSTALL_DATA} ${WRKSRC}/man/${file}.1 \
		${DESTDIR}${PREFIX}/${PKGMANDIR}/man1/${file}${PYVERSSUFFIX}.1
.endfor

do-test:
	cd ${WRKSRC} && pytest-${PYVERSSUFFIX}

.include "../../lang/python/application.mk"
.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
