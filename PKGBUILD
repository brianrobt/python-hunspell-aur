# Maintainer: envolution
# shellcheck shell=bash disable=SC2034,SC2154
pkgname=python-hunspell
pkgver=0.5.5
pkgrel=1
pkgdesc="Python bindings for Hunspell"
arch=('any')
url="https://github.com/pyhunspell/pyhunspell"
license=('GPL-3.0-or-later')
depends=('hunspell')
checkdepends=('python-setuptools')
source=("$pkgname-$pkgver.tar.gz::https://github.com/pyhunspell/pyhunspell/archive/refs/tags/$pkgver.tar.gz"
  pyproject.toml)
sha256sums=('021f2b713ebf1af972655b7f7a7669e96d8e2c59f4c984164b3fc1b7b5e2a51c'
            '3f9203dcf2441ea9d3ef1a6807c9209d2896011c059e96d6914dc21df7194fc2')

build() {
  cd "pyhunspell-$pkgver"
  python setup.py build #yes this is deprectaed, there's no project file so contribute one if you can
}

package() {
  cd "pyhunspell-$pkgver"
  python setup.py install --prefix="$pkgdir/usr"
}
# vim:set ts=2 sw=2 et:
