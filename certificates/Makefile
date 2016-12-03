.include <bsd.own.mk>

FILESDIR= ${PREFIX}/share/certs

PRODUCTION_CERTS=	Production-1.pem Production-2.pem zfstor-update.pem
NIGHTLY_CERTS=	ZFStor-Nightly.pem nightlies-1.pem nightlies-2.pem

FILES=	Production.pem \
	Nightlies.pem \
	zfstor-CA.pem

Production.pem:	${PRODUCTION_CERTS}
	cat ${.ALLSRC} > ${.TARGET}

Nightlies.pem:	${NIGHTLY_CERTS}
	cat ${.ALLSRC} > ${.TARGET}

beforeinstall:
	${INSTALL} -d ${DESTDIR}${FILESDIR}

.include <bsd.lib.mk>

