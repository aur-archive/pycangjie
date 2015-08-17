# Maintainer: Antony Ho <ntonyworkshop@gmail.com>
pkgname=pycangjie
pkgver=1.2
pkgrel=1
pkgdesc="This is a Python wrapper to libcangjie, the library implementing Cangjie and Quick input methods."
arch=('x86_64' 'i686')
url="http://cangjians.github.io/projects/pycangjie/"
license=('LGPL3')
depends=('libcangjie' 'python>=3.2')
makedepends=('cython>=0.17')
replaces=('pycangjie-git')
sha256sums=('bc9115904f65581a11e43044c83e999e583468d1bb98c04b33ea059205e07c10')
source=("https://github.com/Cangjians/$pkgname/releases/download/v$pkgver/cangjie-$pkgver.tar.xz")


check() {
  cd "$srcdir/cangjie-$pkgver"
  make check
}

build() {
  cd "$srcdir/cangjie-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/cangjie-$pkgver"
  make DESTDIR="$pkgdir/" install
}
