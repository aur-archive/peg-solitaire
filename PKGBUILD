# Contributer: giacomogiorgianni@gmail.com

pkgname=peg-solitaire
pkgver=2.0
pkgrel=2
pkgdesc="A free and fun board game also known as English peg solitaire or Senku"
arch=('i686' 'x86_64')
url=("https://opendesktop.org/content/show.php/Peg+Solitaire?content=140433")
license=('GPL')
depends=('qt4')
makedepends=('cmake' 'automoc4')
install=${pkgname}.install
source=("http://sourceforge.net/projects/peg-solitaire/files/version 2.0 (March%2C 2013)/$pkgname-$pkgver.tar.gz")
md5sums=('359eed7ffa1d5f957a9867f24bfce049')

build() {
  cd ${srcdir}/$pkgname-$pkgver
  qmake-qt4 $pkgname.pro -r -config release 
  make clean && make
}

package() {
  cd ${srcdir}/$pkgname-$pkgver
  make INSTALL_ROOT=${pkgdir} install
}
