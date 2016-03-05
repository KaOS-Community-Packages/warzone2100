pkgname=warzone2100
pkgver=3.1.3
pkgrel=1
pkgdesc="3D realtime strategy game on a future Earth"
url="http://wz2100.net/"
arch=('x86_64')
license=('GPL')
depends=('sdl' 'glew' 'fribidi' 'openal' 'libvorbis' 'libtheora' 'physfs' 'ttf-dejavu' 'qt')
makedepends=('gawk' 'flex' 'zip' 'unzip' 'asciidoc' 'mesa')
source=("http://downloads.sourceforge.net/project/warzone2100/releases/${pkgver}/${pkgname}-${pkgver}.tar.xz")
md5sums=('0363cb43f037a5eadab7595bb1ab06e3')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
} 
