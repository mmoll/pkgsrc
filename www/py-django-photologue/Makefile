# $NetBSD: Makefile,v 1.11 2018/03/05 14:13:22 adam Exp $

DISTNAME=	django-photologue-3.8.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	www python
MASTER_SITES=	${MASTER_SITE_PYPI:=d/django-photologue/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/jdriscoll/django-photologue
COMMENT=	Plug-in photo management application for the Django framework
LICENSE=	modified-bsd

DEPENDS+=	${PYPKGPREFIX}-Pillow>=4.3.0:../../graphics/py-Pillow
DEPENDS+=	${PYPKGPREFIX}-django>=1.11:../../www/py-django
DEPENDS+=	${PYPKGPREFIX}-django-sortedm2m>=1.5.0:../../www/py-django-sortedm2m
DEPENDS+=	${PYPKGPREFIX}-exifread>=2.1.2:../../graphics/py-exifread

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
