# $FreeBSD: head/java/linux-oracle-jre18/Makefile 351369 2014-04-15 22:17:02Z jkim $

PORTNAME=	jre
PORTVERSION=	${JRE_VERSION}.${JRE_UPDATE_VERSION}
CATEGORIES=	java
MASTER_SITES=	#
PKGNAMEPREFIX=	linux-oracle-
DISTNAME=	jre-${JRE_VERSION}u${JRE_UPDATE_VERSION}-linux-i586

MAINTAINER=	java@FreeBSD.org
COMMENT=	Oracle Java ${JRE_VERSION} Runtime Environment for Linux

RUN_DEPENDS=	javavm:${PORTSDIR}/java/javavmwrapper

NO_CDROM=	License does not allow distribution with fee
RESTRICTED=	Redistribution of repackaged binaries not permitted
PKGNAMESUFFIX=	1${JRE_VERSION}

WRKSRC=		${WRKDIR}/jre${DL_JRE_VERSION}
PLIST_SUB+=	T=${APP_HOME:S/^${PREFIX}\///} PORTVERSION=${PORTVERSION}

NO_BUILD=	yes
USE_LINUX=	yes
USE_LINUX_APPS=	xorglibs
USES=		shebangfix
ONLY_FOR_ARCHS=	i386 amd64

JRE_VERSION=		8
JRE_INTERNAL_VERSION=	1.${JRE_VERSION}.0
JRE_UPDATE_VERSION=	5
.if ${JRE_UPDATE_VERSION} == 0
DL_JRE_VERSION=		${JRE_INTERNAL_VERSION}
.elif ${JRE_UPDATE_VERSION} <= 9
DL_JRE_VERSION=		${JRE_INTERNAL_VERSION}_0${JRE_UPDATE_VERSION}
.else
DL_JRE_VERSION=		${JRE_INTERNAL_VERSION}_${JRE_UPDATE_VERSION}
.endif
DOWNLOAD_URL=		http://www.oracle.com/technetwork/java/javase/downloads/index.html

APP_HOME=	${PREFIX}/${PKGNAMEPREFIX}${PORTNAME}${JRE_INTERNAL_VERSION}
BIN_DIRS=	bin
SHEBANG_FILES=	bin/jcontrol
bash_CMD=	${SH}

.include <bsd.port.pre.mk>

.if !exists(${DISTDIR}/${DISTNAME}${EXTRACT_SUFX})
IGNORE?=You must manually fetch the J2SE RE download for the Linux platform (${DISTNAME}${EXTRACT_SUFX}) from ${DOWNLOAD_URL}, place it in ${DISTDIR} and then run make again
.endif

do-install:
	@${MKDIR} ${STAGEDIR}${APP_HOME}
	@cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}${APP_HOME}
	@cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}${APP_HOME} \
	    "-not ( -type d -name bin -prune )"
	@cd ${WRKSRC} && ${COPYTREE_BIN} "${BIN_DIRS}" ${STAGEDIR}${APP_HOME}
	@${INSTALL_SCRIPT} ${WRKSRC}/lib/jexec ${STAGEDIR}${APP_HOME}/lib

.include <bsd.port.post.mk>
