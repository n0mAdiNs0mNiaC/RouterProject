# Created by: Johannes Meixner <johannes@perceivon.net>
# $FreeBSD$

PORTNAME=	sdl_ttf
PORTVERSION=	2.0.11
DISTVERSIONSUFFIX=	-6.el6
PORTREVISION=	4
CATEGORIES=	graphics linux
MASTER_SITES=	EPEL/s
DISTNAME=	SDL_ttf-${DISTVERSIONFULL}

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Simple library to load True Type Fonts as SDL interfaces (Linux CentOS ${LINUX_DIST_VER})

USES=		linux:c6
USE_LDCONFIG=	yes
USE_LINUX=	jpeg png sdl12 tiff
USE_LINUX_RPM=	yes

DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr
DOCSDIR=	${PREFIX}/usr/share/doc/SDL_ttf-${PORTVERSION}

OPTIONS_DEFINE=	DOCS

.include <bsd.port.mk>
