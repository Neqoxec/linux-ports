# Created by: Johannes Meixner <xmj@chaot.net>
# $FreeBSD$

PORTNAME=	esound
PORTVERSION=	0.2.41
CATEGORIES=	audio linux
DISTNAME=	${PORTNAME}-libs-${PORTVERSION}-${RPMVERSION}

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	RPM of esound (Linux CentOS ${LINUX_DIST_VER})

CONFLICTS=	linux-esound-[0-9]* linux-f10-esound-[0-9]*

USE_LINUX=	yes
USE_LINUX_RPM=	yes
USE_LINUX_APPS=	libaudiofile
LINUX_NAME=	${PORTNAME}-libs

RPMVERSION=	3.1.el6
USE_LDCONFIG=	yes
SRC_DISTFILES=	${PORTNAME}-${PORTVERSION}-${RPMVERSION}

PLIST_FILES=	usr/lib/libesd.so.0 usr/lib/libesd.so.0.2.39 \
		usr/lib/libesddsp.so.0 usr/lib/libesddsp.so.0.2.39
DOCSDIR=	${PREFIX}/usr/share/doc/${LINUX_NAME}-${PORTVERSION}
PORTDOCS=	AUTHORS COPYING.LIB ChangeLog NEWS README TIPS TODO esound.sgml
DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr

.include <bsd.port.mk>
