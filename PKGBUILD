# Maintainer: BasioMeusPuga <disgruntled.mob@gmail.com>

pkgname=lector
_pkgname=Lector
pkgdesc="Qt based ebook reader"
pkgver=0.5
pkgrel=1
arch=('any')
url="https://github.com/BasioMeusPuga/Lector"
license=('GPL3')
provides=('lector')
conflicts=('lector')
depends=('qt5-base' 'qt5-multimedia' 'python' 'python-pyqt5' 'python-beautifulsoup4' 'python-lxml' 'poppler-qt5' 'python-poppler-qt5')
makedepends=('git' 'python-setuptools')

source=("$pkgname-$pkgver.tar.gz::https://github.com/BasioMeusPuga/$_pkgname/archive/$pkgver.tar.gz")
sha512sums=('b6a41a7d072d6cac79245233c49bd16dc527a58d91d8c7765037917de8048519bd6dd23b300b6aa747bebabb81ce725d96270eac84bfa0d1d5d19d1dcbbb9ead')

build() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py build
}

package() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py install --root="$pkgdir" --optimize=1
}
