pkgname=warzone2100
pkgver=3.1.2
pkgrel=1
pkgdesc="3D realtime strategy game on a future Earth"
url="http://wz2100.net/"
arch=('x86_64')
license=('GPL')
depends=('sdl' 'glew' 'fribidi' 'openal' 'libvorbis' 'libtheora' 'physfs' 'ttf-dejavu' 'qt')
makedepends=('gawk' 'flex' 'zip' 'unzip' 'asciidoc' 'mesa')
source=("http://downloads.sourceforge.net/project/warzone2100/releases/${pkgver}/${pkgname}-${pkgver}.tar.xz"
        'buildfix.patch')
md5sums=('4e947125e9604821164f1ad9d1922447'
         '195dc8e8c186421b91d1868424440c27')

prepare() {
  cd ${pkgname}-${pkgver}

  patch -p1 -i ../buildfix.patch
}

build() {
  cd ${pkgname}-${pkgver}

  ./configure --prefix=/usr --with-distributor="Archlinux"

  make
}

package() {
  cd ${pkgname}-${pkgver}

  make DESTDIR=${pkgdir} install
} 
