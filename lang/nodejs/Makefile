# $NetBSD: Makefile,v 1.140 2018/08/02 12:18:24 fhajny Exp $

DISTNAME=	node-v10.8.0

USE_LANGUAGES=	c gnu++14

# Stated by the changelog as of 8.2.0
GCC_REQD+=	4.9.4

.include "../../mk/bsd.prefs.mk"

# Optional OpenSSL support in nghttp2 conflicts with OpenSSL 1.1.x
# bundled and built by lang/nodejs.
# Uncomment when we switch to openssl>=1.1
# CONFIGURE_ARGS+=	--shared-nghttp2
CONFIGURE_ARGS+=	--with-intl=system-icu

CHECK_PORTABILITY_SKIP+=	deps/openssl/openssl/.travis-create-release.sh

.include "options.mk"

.include "../../lang/nodejs/Makefile.common"
.include "../../textproc/icu/buildlink3.mk"
# Uncomment when we switch to openssl>=1.1
# .include "../../www/nghttp2/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
