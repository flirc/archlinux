# Maintainer: Jonathan Steel <jsteel at archlinux.org>
# Contributor: cornholio <vigo.the.unholy.carpathian@gmail.com>
# Contributor: Michael Mansell <michael.mansell@gmail.com>
# Contributor: Marcin Jaworski <marcin@jaworski.me>

pkgname=flirc-bin
_pkgname=flirc
_pkgver=3.9.7
pkgver=${_pkgver/-/.}
pkgrel=1
pkgdesc="CLI and GUI application to program your Flirc device"
arch=('x86_64')
url="http://flirc.tv"
license=('unknown')
depends=('qt4' 'libusb' 'hidapi')
provides=('flirc')
conflicts=('flirc')
replaces=('flirc')
source_x86_64+=("${_pkgname}_${_pkgver}_amd64.deb::https://packagecloud.io/Flirc/repo/packages/ubuntu/zesty/${_pkgname}_${_pkgver}_amd64.deb/download.deb")
sha256sums_x86_64=('0e33025896a6be60f944f1d8744e563a25503571ad0826a14539c706c81ad490')

package() {
  tar -xf data.tar.gz -C "$pkgdir"
  rm -f "$pkgdir/usr/bin/.gitignore"
  find "$pkgdir" -mindepth 1 -type d -exec chmod 755 {} \;
}
