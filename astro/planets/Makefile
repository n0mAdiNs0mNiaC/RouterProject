# Created by: Ying-Chieh Liao <ijliao@FreeBSD.org>
# $FreeBSD$

PORTNAME=	planets
PORTVERSION=	0.1.13
PORTREVISION=	1
CATEGORIES=	astro
MASTER_SITES=	GENTOO \
		http://planets.homedns.org/dist/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Orbital simulator

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		unfetchable
DEPRECATED=	Unfetchable, unmaintained
EXPIRATION_DATE=	2019-10-16

USES=		gmake tar:tgz
USE_OCAML=	yes
USE_OCAML_CAMLP4=yes
USE_OCAML_TK=	yes
USE_XORG=	x11
ALL_TARGET=	${PORTNAME}

OPTIONS_DEFINE=	DOCS

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/planets.1 ${STAGEDIR}${MANPREFIX}/man/man1

do-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/KEYBINDINGS.txt ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/getting_started.html ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
