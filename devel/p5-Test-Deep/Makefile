# $NetBSD: Makefile,v 1.34 2018/05/02 12:09:53 wiz Exp $

DISTNAME=		Test-Deep-1.128
PKGNAME=		p5-${DISTNAME}
CATEGORIES=		devel perl5
MASTER_SITES=		${MASTER_SITE_PERL_CPAN:=../../authors/id/R/RJ/RJBS/}

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		http://search.cpan.org/dist/Test-Deep/
COMMENT=		Perl5 module to test deep structures
LICENSE=		${PERL5_LICENSE}

DEPENDS+=		p5-Test-Simple>=1.001010:../../devel/p5-Test-Simple

PERL5_PACKLIST=		auto/Test/Deep/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
