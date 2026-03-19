# Maintainer: artist for Sonic-DE

pkgname=sonic-workspace-wallpapers
pkgver=6.6.3
_dirver=$(echo $pkgver | cut -d. -f1-3)
pkgrel=1
pkgdesc='Additional wallpapers for the Sonic Workspace'
arch=(any)
url='https://github.com/Sonic-DE/sonic-workspace-wallpapers'
license=(LGPL)
makedepends=(extra-cmake-modules qt5-base)
groups=(sonicde)
conflicts=(plasma-workspace-wallpapers)
provides=(plasma-workspace-wallpapers)
source=("$pkgname-$pkgver.tar.gz::${url}/archive/refs/tags/$_dirver.tar.gz")

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DBUILD_TESTING=OFF
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}

sha256sums=('0f3f2b853cc0fb2bb0372bb1b255575e79821ccccb3c748db5dca3511f0ff386')

