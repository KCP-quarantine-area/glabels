pkgname=glabels
pkgver=3.4.0
pkgrel=1
pkgdesc="Creating labels and business cards the very easy way"
arch=('x86_64')
url="http://glabels.org/"
license=('GPL' 'LGPL')
depends=('qrencode')
makedepends=('intltool' 'itstool')
source=(https://download.gnome.org/sources/$pkgname/${pkgver%.*}/$pkgname-$pkgver.tar.xz)
sha256sums=('d40e079395d30adbcd8204f41d08f7a8da9ec130bffa4cb3c130fbe2322b6410')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var \
              --disable-schemas-compile
  make
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}
