# $NetBSD: Makefile,v 1.2 2018/06/16 14:45:32 bsiegert Exp $

DISTNAME=	gcs-oauth2-boto-plugin-2.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	net
MASTER_SITES=	${MASTER_SITE_PYPI:=g/gcs-oauth2-boto-plugin/}

MAINTAINER=	bsiegert@NetBSD.org
HOMEPAGE=	https://github.com/GoogleCloudPlatform/gcs-oauth2-boto-plugin
COMMENT=	Boto auth plugin for Google Cloud Storage
LICENSE=	apache-2.0

DEPENDS+=	${PYPKGPREFIX}-boto>=2.29.1:../../net/py-boto
DEPENDS+=	${PYPKGPREFIX}-httplib2>=0.8:../../www/py-httplib2
DEPENDS+=	${PYPKGPREFIX}-google-reauth>=0.1.0:../../security/py-google-reauth
DEPENDS+=	${PYPKGPREFIX}-oauth2client>=2.2.0:../../security/py-oauth2client
DEPENDS+=	${PYPKGPREFIX}-OpenSSL>=0.13:../../security/py-OpenSSL
DEPENDS+=	${PYPKGPREFIX}-retry_decorator>=1.0.0:../../devel/py-retry_decorator
DEPENDS+=	${PYPKGPREFIX}-six>=1.6.1:../../lang/py-six
DEPENDS+=	${PYPKGPREFIX}-SocksiPy-branch-1.01*:../../net/py-socksipy-branch

# Test dependencies:
DEPENDS+=	${PYPKGPREFIX}-freezegun-[0-9]*:../../devel/py-freezegun
DEPENDS+=	${PYPKGPREFIX}-mock-[0-9]*:../../devel/py-mock

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
