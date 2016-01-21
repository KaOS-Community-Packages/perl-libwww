pkgname=perl-libwww
pkgver=6.15
pkgrel=1
pkgdesc="The World-Wide Web library for Perl"
arch=('x86_64')
url="https://metacpan.org/release/libwww-perl"
license=('PerlArtistic' 'GPL')
depends=('perl' 'perl-encode-locale' 'perl-file-listing'
         'perl-html-parser' 'perl-http-cookies' 'perl-http-daemon'
         'perl-http-date' 'perl-http-negotiate' 'perl-lwp-mediatypes'
         'perl-net-http' 'perl-uri' 'perl-www-robotrules'
         'perl-http-message')
optdepends=('perl-lwp-protocol-https: for https:// url schemes')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/E/ET/ETHER/libwww-perl-${pkgver}.tar.gz)
sha1sums=('9e27f58108135b7871bbe406e39353a1dbc99462')

build() {
  cd libwww-perl-${pkgver}
  perl Makefile.PL --aliases INSTALLDIRS=vendor
  make
}

check()  {
  cd libwww-perl-${pkgver}
  make test
}

package() {
  cd libwww-perl-${pkgver}
  make DESTDIR="$pkgdir" install
}
