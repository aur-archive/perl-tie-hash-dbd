# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-tie-hash-dbd'
pkgver='0.10'
pkgrel='1'
pkgdesc=""
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-dbi>=1.613')
makedepends=()
url='http://search.cpan.org/dist/Tie-Hash-DBD'
source=('http://search.cpan.org/CPAN/authors/id/H/HM/HMBRAND/Tie-Hash-DBD-0.10.tgz')
md5sums=('a2bb4c5c8c3c7afb06cb1a81aa40a45d')
sha512sums=('70bfaa135452006709b2201c2ecbaba1752d5085906df3b8315e9e816246c591b05f8acc7a9e9d0a3aa5129f9a71608fb262c2aa5f34af47d276dad98a24c7fd')
_distdir="Tie-Hash-DBD-0.10"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
