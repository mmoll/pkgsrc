# $NetBSD: Makefile,v 1.21 2018/05/17 13:06:13 leot Exp $

DISTNAME=	mitmproxy-4.0.1
CATEGORIES=	net
MASTER_SITES=	${MASTER_SITE_GITHUB:=mitmproxy/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	leot@NetBSD.org
HOMEPAGE=	https://mitmproxy.org/
COMMENT=	Interactive console program for inspecting and editing traffic flows
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-OpenSSL>=17.5:../../security/py-OpenSSL
DEPENDS+=	${PYPKGPREFIX}-asn1>=0.3.1:../../security/py-asn1
DEPENDS+=	${PYPKGPREFIX}-blinker>=1.4:../../devel/py-blinker
DEPENDS+=	${PYPKGPREFIX}-brotlipy>=0.7.0:../../archivers/py-brotlipy
DEPENDS+=	${PYPKGPREFIX}-certifi>=2015.11.20.1:../../security/py-certifi
DEPENDS+=	${PYPKGPREFIX}-click>=6.2:../../devel/py-click
DEPENDS+=	${PYPKGPREFIX}-cryptography>=2.1.4:../../security/py-cryptography
DEPENDS+=	${PYPKGPREFIX}-h2>=3.0.1:../../www/py-h2
DEPENDS+=	${PYPKGPREFIX}-hyperframe>=5.1.0:../../www/py-hyperframe
DEPENDS+=	${PYPKGPREFIX}-kaitaistruct>=0.7:../../devel/py-kaitaistruct
DEPENDS+=	${PYPKGPREFIX}-ldap3>=2.5:../../databases/py-ldap3
DEPENDS+=	${PYPKGPREFIX}-passlib>=1.6.5:../../security/py-passlib
DEPENDS+=	${PYPKGPREFIX}-pyparsing>=2.1.3:../../devel/py-pyparsing
DEPENDS+=	${PYPKGPREFIX}-pyperclip>=1.6.0:../../x11/py-pyperclip
DEPENDS+=	${PYPKGPREFIX}-ruamel-yaml>=0.13.2:../../devel/py-ruamel-yaml
DEPENDS+=	${PYPKGPREFIX}-sortedcontainers>=1.5.4:../../devel/py-sortedcontainers
DEPENDS+=	${PYPKGPREFIX}-tornado>=4.3.0:../../www/py-tornado
DEPENDS+=	${PYPKGPREFIX}-urwid>=2.0.1:../../devel/py-urwid
DEPENDS+=	${PYPKGPREFIX}-wsproto>=0.11.0:../../www/py-wsproto

REPLACE_SH+=	mitmproxy/contrib/kaitaistruct/make.sh

USE_LANGUAGES=			# none
PYTHON_VERSIONS_INCOMPATIBLE=	27 34 35

.include "../../lang/python/application.mk"
.include "../../lang/python/distutils.mk"
.include "../../mk/bsd.pkg.mk"
