# Created by: Stas Timoklhin <devel@stasyan.com>
# $FreeBSD: head/security/linux-f10-libgpg-error/Makefile 340722 2014-01-22 17:00:46Z mat $

PORTNAME=	libgpg-error
PORTVERSION=	1.6
PORTREVISION=	1
CATEGORIES=	security linux

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	Common error values for all GnuPG components

USE_LINUX=	f10
USE_LINUX_RPM=	yes

RPMVERSION=	2
USE_LDCONFIG=	yes
BRANDELF_FILES=	usr/bin/gpg-error

PLIST_SUB=	PORTVERSION="${PORTVERSION}"
DESCR=		${.CURDIR}/../libgpg-error/pkg-descr

.include <bsd.port.mk>
