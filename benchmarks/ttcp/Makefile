# Created by: mharo@FreeBSD.org
# $FreeBSD$

PORTNAME=	ttcp
PORTVERSION=	1.12
PORTREVISION=	1
CATEGORIES=	benchmarks net
MASTER_SITES=	ftp://ftp.sgi.com/sgi/src/ttcp/
DISTFILES=	ttcp.c ttcp.1 README
DIST_SUBDIR=	${PORTNAME}
EXTRACT_ONLY=	# none

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Benchmarking tool for analysing TCP and UDP performance

LICENSE=	PD

BROKEN=		unfetchable
DEPRECATED=	Unfetchable, unmaintained
EXPIRATION_DATE=	2019-10-16

NO_WRKSUBDIR=	yes

OPTIONS_DEFINE=	DOCS

post-extract:
	${CP} ${DISTDIR}/${DIST_SUBDIR}/ttcp.c ${WRKSRC}
	${CP} ${DISTDIR}/${DIST_SUBDIR}/ttcp.1 ${WRKSRC}
	${CP} ${DISTDIR}/${DIST_SUBDIR}/README ${WRKSRC}

do-build:
	${CC} ${CFLAGS} -o ${WRKSRC}/ttcp ${WRKSRC}/ttcp.c

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/ttcp ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/ttcp.1 ${STAGEDIR}${MAN1PREFIX}/man/man1

do-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/README ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
