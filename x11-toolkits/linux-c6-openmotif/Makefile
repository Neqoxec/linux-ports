# Created by: Johannes Meixner <xmj@chaot.net>
# $FreeBSD$

PORTNAME=	openmotif
PORTVERSION=	2.3.3
CATEGORIES=	x11-toolkits linux

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Motif toolkit libraries (Linux CentOS ${LINUX_DIST_VER})

CONFLICTS=	linux-openmotif-[0-9]* linux-f8-openmotif-[0-9]*

ONLY_FOR_ARCHS=	i386 amd64
USE_LINUX=	yes
RPMVERSION=	6.1.el6_4
USE_LINUX_RPM=	yes
USE_LINUX_APPS=	xorglibs
USE_LDCONFIG=	yes
DESCR=	${.CURDIR}/../open-motif/pkg-descr

post-extract:
		@${RM} -r ${WRKSRC}/etc ${WRKSRC}/usr/bin ${WRKSRC}/usr/include \
			${WRKSRC}/usr/share

.include <bsd.port.mk>
