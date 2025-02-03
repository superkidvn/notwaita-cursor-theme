# Maintainer: Kiet Huynh <11086238+superkidvn@users.noreply.github.com>

pkgname=notwaita-cursor-theme-bin
pkgver=1.0.0_alpha1
pkgrel=1
pkgdesc="A cursor theme inspired by the Adwaita icons from the GNOME Project for Windows and Linux with HiDPI support."
arch=('x86_64')
url="https://github.com/ful1e5/notwaita-cursor"
license=('LGPL-3.0-only')
provides=("${pkgname%-bin}")
conflicts=("${pkgname%-bin}")
source=(${pkgname%-bin}-${pkgver//_/-}.tar.xz::"${url}/releases/download/v${pkgver//_/-}/Notwaita.tar.xz"
        LICENSE::"${url//github.com/raw.githubusercontent.com}/refs/heads/main/COPYING_LGPL")
sha256sums=('93928d9c64e2aa61e061efcfbdbf67ae15c458095c6d82f5ad790a1402d46cf2'
            'da7eabb7bafdf7d3ae5e9f223aa5bdc1eece45ac569dc21b3b037520b4464768')
prepare(){
  tar -xf "${pkgname%-bin}-${pkgver//_/-}.tar.xz"
}

package() {
  mkdir -p "${pkgdir}/usr/share/icons"
  cp -r Notwaita-* "${pkgdir}/usr/share/icons"
}
