# Maintainer: BasioMeusPuga <disgruntled.mob@gmail.com>

pkgname=lector
_pkgname=Lector
pkgdesc="Qt based ebook reader"
pkgver=0.5.1
pkgrel=1
arch=('any')
url="https://github.com/BasioMeusPuga/Lector"
license=('GPL3')
provides=('lector')
conflicts=('lector')
depends=('qt5-base' 'qt5-multimedia' 'python' 'python-pyqt5' 'python-beautifulsoup4' 'python-lxml' 'poppler-qt5' 'python-poppler-qt5')
makedepends=('git' 'python-setuptools')

source=("$pkgname-$pkgver.tar.gz::https://github.com/BasioMeusPuga/$_pkgname/archive/$pkgver.tar.gz")
sha512sums=('6b55a3888d5eb1902f966bccd693f1c3fba8d936e750e09dabfb120a372f4e16befed79d5b3031ad4b66e678bfb2597e30c35e1e59f9db1bdf27f1facad0ee4d')

build() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py build
}

package() {
    cd "$srcdir/$_pkgname-$pkgver"
    python setup.py install --root="$pkgdir" --optimize=1
}
