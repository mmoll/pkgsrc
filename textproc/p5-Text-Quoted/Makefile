# $NetBSD: Makefile,v 1.26 2018/08/01 07:05:29 wen Exp $
#

DISTNAME=	Text-Quoted-2.10
PKGNAME=	p5-${DISTNAME}
CATEGORIES=	textproc perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Text/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/Text-Quoted/
COMMENT=	Extract the structure of a quoted mail message
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Text-Autoformat>=1.04:../../textproc/p5-Text-Autoformat

USE_LANGUAGES=		# empty
PERL5_PACKLIST=		auto/Text/Quoted/.packlist
PERL5_MODULE_TYPE=	Module::Install::Bundled

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
