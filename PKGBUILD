# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=ehaskell
pkgname=ehaskell
pkgver=0.7
pkgrel=3
pkgdesc="like eruby, ehaskell is embedded haskell."
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-directory=1.0.1.1' 'haskell-filepath=1.1.0.4' 'haskell-mtlparse>=0.0.1' 'haskell-process=1.0.1.3' 'haskell-regexpr>=0.3.3' 'haskell-utf8-string' 'haskell-yjtools>=0.8')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('487e42dff8e0d4f88f27942216b063b0')
