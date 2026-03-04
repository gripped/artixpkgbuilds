# Maintainer: Artist for XLibre

pkgname=sonic-silver-sddm
_pkgname="${pkgname#*-}"
pkgver=0.1
pkgrel=2
_commit="8b3c56d815bd13d242301e1f8be23a7c95"
pkgdesc="Sonic Silver SDDM Theme (KDE Plasma 6)"
arch=(x86_64)
url="https://github.com/Sonic-DE/${_pkgname}"
license=('LGPL-2.0-or-later')
depends=(sonic-workspace)
makedepends=(git)
groups=(sonicde)
source=("git+${url}.git#commit=$_commit")

package() {
  cd "${_pkgname}"
  install -d "$pkgdir/usr/share/sddm/themes"
  cp -rv Sonic-Silver "${pkgdir}/usr/share/sddm/themes"
  cp -rv Sonic-Silver-Light "${pkgdir}/usr/share/sddm/themes"

  install -Dm644 -t "$pkgdir/usr/share/doc/$pkgname" CHANGELOG README.md
  install -Dm644 -t "$pkgdir/usr/share/licenses/$pkgname" LICENSE.md
}

sha256sums=('8c32ef6a026c665ee215d8b13bb6420fc5a09f6898460dffdc060347776d5a44')
