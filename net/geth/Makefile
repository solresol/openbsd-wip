# $OpenBSD: Makefile.template,v 1.76 2017/02/25 16:04:20 danj Exp $

COMMENT =	go implementation of the ethereum protocol
GH_ACCOUNT =	ethereum
GH_PROJECT =	go-ethereum
GH_TAGNAME =	v1.8.12

CATEGORIES =	net

HOMEPAGE =	https://geth.ethereum.org/

WANTLIB += c pthread

# MIT
PERMIT_PACKAGE_CDROM = Yes

MODULES =	lang/go
MODGO_TYPE =	bin

do-build:
	cd ${WRKSRC} && make all

do-install:
	for b in abigen bootnode evm geth puppeth rlpdump swarm wnode ; do \
		${INSTALL_PROGRAM} ${WRKSRC}/build/bin/$$b ${PREFIX}/bin/; \
	done

.include <bsd.port.mk>
