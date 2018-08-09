# Maintainer: BasioMeusPuga <disgruntled.mob@gmail.com>

pkgname=lector
_pkgname=Lector
pkgdesc="Qt based ebook reader"
pkgver=0.4
pkgrel=2
arch=('any')
url="https://github.com/BasioMeusPuga/Lector"
license=('GPL3')
provides=('lector')
conflicts=('lector')
depends=('qt5-base' 'qt5-multimedia' 'python' 'python-pyqt5' 'python-beautifulsoup4' 'python-lxml' 'poppler-qt5' 'python-poppler-qt5')
makedepends=('git' 'python-setuptools')

source=("$pkgname-$pkgver.tar.gz::https://github.com/BasioMeusPuga/$_pkgname/archive/$pkgver.tar.gz")
sha512sums=('791165d8e61af145c770d5ff5b77c1bb4b738f9e05e7321d43ae928e63d4f7d0fa07e7389b17c7944ee377d704be4a3862105388e6d721378851b735a287b050')

build() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py build
}

package() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py install --root="$pkgdir" --optimize=1
}
