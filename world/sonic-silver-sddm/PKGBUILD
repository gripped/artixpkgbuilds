# Maintainer: Artist for XLibre

pkgname=sonic-silver-sddm
_pkgname="${pkgname#*-}"
pkgver=1.0.0
pkgrel=1
pkgdesc="Sonic Silver SDDM Theme (KDE Plasma 6)"
arch=(x86_64)
url="https://github.com/Sonic-DE/${_pkgname}"
license=('LGPL-2.0-or-later')
depends=(sonic-workspace)
groups=(sonicde)
source=("${pkgver}-${_pkgname}.tag.gz::${url}/archive/refs/tags/${pkgver}.tar.gz")

package() {
  cd "${_pkgname}-${pkgver}"
  install -d "$pkgdir/usr/share/sddm/themes"
  cp -rv Sonic-Silver "${pkgdir}/usr/share/sddm/themes"
  cp -rv Sonic-Silver-Light "${pkgdir}/usr/share/sddm/themes"

  install -Dm644 -t "$pkgdir/usr/share/doc/$pkgname" CHANGELOG README.md
  install -Dm644 -t "$pkgdir/usr/share/licenses/$pkgname" LICENSE.md
}

sha256sums=('3c32317306a723a0cdbffb41ebb0e817e46527c8f2ebdfd1cd1f304ee6d3a235')
