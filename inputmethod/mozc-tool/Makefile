# $NetBSD: Makefile,v 1.38 2018/07/20 03:34:17 ryoon Exp $

PKGNAME=	${DISTNAME:S/mozc-/mozc-tool-/}
PKGREVISION=	7

INSTALLATION_DIRS+=	libexec

ALL_ENV+=	qt_dir=${QTDIR}

do-build:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} \
		${PYTHONBIN} build_mozc.py build -c ${MOZC_BUILD_MODE} \
			gui/gui.gyp:mozc_tool

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/out_${OSDEST}/${MOZC_BUILD_MODE}/mozc_tool \
		${DESTDIR}${PREFIX}/libexec

.include "../../inputmethod/mozc-server/Makefile.common"
