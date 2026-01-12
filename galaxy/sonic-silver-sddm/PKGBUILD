# Maintainer: Artist for XLibre

pkgname=sonic-silver-sddm
_pkgname="${pkgname#*-}"
pkgver=0.1
pkgrel=1
pkgdesc="Sonic Silver SDDM Theme (KDE Plasma 6)"
arch=(x86_64)
url="https://github.com/Sonic-DE/${_pkgname}"
license=('LGPL-2.0-or-later')
depends=(plasma-workspace)
makedepends=(git)
groups=(sonicde)
source=("git+${url}.git")

package() {
  cd "${_pkgname}"
  install -d "$pkgdir/usr/share/sddm/themes"
  cp -rv Sonic-Silver "${pkgdir}/usr/share/sddm/themes"
  cp -rv Sonic-Silver-Light "${pkgdir}/usr/share/sddm/themes"

  install -Dm644 -t "$pkgdir/usr/share/doc/$pkgname" CHANGELOG README.md
  install -Dm644 -t "$pkgdir/usr/share/licenses/$pkgname" LICENSE.md
}

sha256sums=('SKIP')
