# Maintainer: gravskrift <gravskrift@gmail.com>
pkgname=zeeb
pkgver=3.9.24
pkgrel=1
pkgdesc="Adobe AIR app for renaming movie files & DVD folders."
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/zeeb/"
license=('unknown')
depends=('adobe-air')
makedepends=('unzip')
source=("http://zeeb.googlecode.com/files/${pkgname}.v${pkgver}.air"
		"${pkgname}.sh"
		"${pkgname}.desktop")
md5sums=('c847f9dadd88b7e15326ebb206fdbce5'
         '628ecd63374ebac66ff0ceaa54593cdb'
         '6a38ab97b56c51f7c42c13be24f8accc')
noextract=(${pkgname}.v${pkgver}.air)

build() {
  cd ${srcdir}
  install -d ${pkgdir}/{opt/${pkgname},usr/{bin,share/{applications,pixmaps/${pkgname}}}}
  unzip ${pkgname}.v${pkgver}.air -d ${srcdir}
  install -Dm644 ${pkgname}.v${pkgver}.air ${pkgdir}/opt/${pkgname}/${pkgname}.air
  install -Dm644 assets/icon/${pkgname}128.png ${pkgdir}/usr/share/pixmaps/${pkgname}.png
  install -Dm644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
  install -Dm755 ${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
}
