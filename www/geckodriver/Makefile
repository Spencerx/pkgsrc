# $NetBSD: Makefile,v 1.4 2018/05/09 23:41:39 maya Exp $

DISTNAME=	geckodriver-0.20.1
CATEGORIES=	www
MASTER_SITES=	${MASTER_SITE_GITHUB:=mozilla/}
GITHUB_PROJECT=	geckodriver
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	tnn@NetBSD.org
HOMEPAGE=	https://github.com/mozilla/geckodriver/
COMMENT=	W3C WebDriver-compatible proxy for Gecko-based browsers
LICENSE=	mpl-1.1

BUILD_DEPENDS+=	rust-[0-9]*:../../lang/rust

CARGO_CRATE_DEPENDS+=		\
	adler32-1.0.2		\
	aho-corasick-0.6.4	\
	base64-0.6.0		\
	bitflags-1.0.1		\
	build_const-0.2.0	\
	byteorder-1.2.2		\
	bzip2-0.3.2		\
	bzip2-sys-0.1.6		\
	cc-1.0.9		\
	cfg-if-0.1.2		\
	chrono-0.2.25		\
	clap-2.31.2		\
	cookie-0.10.1		\
	crc-1.7.0		\
	flate2-1.0.1		\
	fuchsia-zircon-0.3.3	\
	fuchsia-zircon-sys-0.3.3	\
	httparse-1.2.4		\
	hyper-0.10.13		\
	idna-0.1.4		\
	kernel32-sys-0.2.2	\
	language-tags-0.2.2	\
	lazy_static-1.0.0	\
	libc-0.2.40		\
	log-0.3.9		\
	log-0.4.1		\
	matches-0.1.6		\
	memchr-2.0.1		\
	mime-0.2.6		\
	miniz_oxide-0.1.2	\
	miniz_oxide_c_api-0.1.2	\
	mozprofile-0.3.0	\
	mozrunner-0.6.1		\
	mozversion-0.1.3	\
	msdos_time-0.1.5	\
	num-0.1.42		\
	num-integer-0.1.36	\
	num-iter-0.1.35		\
	num-traits-0.2.2	\
	num_cpus-1.8.0		\
	percent-encoding-1.0.1	\
	podio-0.1.6		\
	rand-0.3.22		\
	rand-0.4.2		\
	redox_syscall-0.1.37	\
	regex-0.2.10		\
	regex-syntax-0.5.3	\
	remove_dir_all-0.5.0	\
	rust-ini-0.10.3		\
	rustc-serialize-0.3.24	\
	safemem-0.2.0		\
	semver-0.6.0		\
	semver-parser-0.7.0	\
	strsim-0.7.0		\
	tempdir-0.3.7		\
	term_size-0.3.1		\
	textwrap-0.9.0		\
	thread_local-0.3.5	\
	time-0.1.39		\
	traitobject-0.1.0	\
	typeable-0.1.2		\
	ucd-util-0.1.1		\
	unicase-1.4.2		\
	unicode-bidi-0.3.4	\
	unicode-normalization-0.1.5	\
	unicode-segmentation-1.2.0	\
	unicode-width-0.1.4	\
	unreachable-1.0.0	\
	url-1.7.0		\
	utf8-ranges-1.0.0	\
	uuid-0.1.18		\
	version_check-0.1.3	\
	void-1.0.2		\
	webdriver-0.35.0	\
	winapi-0.2.8		\
	winapi-0.3.4		\
	winapi-build-0.1.1	\
	winapi-i686-pc-windows-gnu-0.4.0	\
	winapi-x86_64-pc-windows-gnu-0.4.0	\
	winreg-0.5.0		\
	zip-0.3.1

do-build:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} ${PREFIX}/bin/cargo build --locked --frozen --release

do-install:
	${INSTALL_PROGRAM_DIR} ${DESTDIR}${PREFIX}/bin
	${INSTALL_PROGRAM} ${WRKSRC}/target/release/geckodriver ${DESTDIR}${PREFIX}/bin

.include "../../lang/rust/cargo.mk"
.include "../../mk/bsd.pkg.mk"
