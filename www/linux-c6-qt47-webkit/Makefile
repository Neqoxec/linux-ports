# Created by: Artyom Mirgorodskiy <artyom.mirgorodsky@gmail.com>
# $FreeBSD$

PORTNAME=	qt47-webkit
PORTVERSION=	4.7.2

MAINTAINER=	emulation@FreeBSD.org

COMMENT=	RPM of QT4 (Linux CentOS 5)

MASTER_SITES=	${MASTER_SITE_LOCAL}
MASTER_SITE_SUBDIR=	xmj
PKGNAMEPREFIX=	linux-${USE_LINUX}-
DISTNAME=	${PORTNAME}-${PORTVERSION}-${RPMVERSION}
SRC_DISTFILES:=		# unretrievable
DIST_SUBDIR=	rpm/${LINUX_RPM_ARCH}/centos/c5

ONLY_FOR_ARCHS=	i386 amd64
RPMVERSION=	1_18.el5
USE_LINUX=	yes
LINUX_RPM_ARCH=	i386
USE_LINUX_APPS=	fontconfig png xorglibs sqlite3 qt47 qt47-x11

CATEGORIES=	www linux
USE_LINUX_RPM=	yes
LINUX_DIST_VER=	5
USE_LDCONFIG=	yes
DESCR=  ${.CURDIR}/../../www/webkit-gtk3/pkg-descr # contains no GTK references, reuse

.include <bsd.port.mk>
