# Created by: Zach Leslie <ports@zleslie.info>

PORTNAME=	freebsd_exporter
PORTVERSION=	0.2.1
PORTREVISION=	1
DISTVERSIONPREFIX=v
CATEGORIES=	sysutils

MAINTAINER=	zach@zleslie.info
COMMENT=	Prometheus Exporter for FreeBSD

LICENSE=	MIT

BUILD_DEPENDS=	git:devel/git

USES=		go:modules
USE_GITHUB=	yes

GH_ACCOUNT=	xaque208

GO_PKGNAME=	github.com/${GH_ACCOUNT}/${PORTNAME}
GO_TARGET=	github.com/${GH_ACCOUNT}/${PORTNAME}
GO_BUILDFLAGS=	-ldflags='-X main.Version=v${PORTVERSION}'

PLIST_FILES=	bin/freebsd_exporter

USE_RC_SUBR=	freebsd_exporter

do-install:
	${INSTALL_PROGRAM} ${WRKDIR}/bin/freebsd_exporter ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
