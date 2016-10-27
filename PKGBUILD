# Maintainer: Tom Ashley <tom.ashley[at]dataloop[dot]io>
pkgname=dataloop-agent
pkgver=1.3.11
pkgrel=1
pkgdesc="The Full stack Dataloop Agent"
url="http://www.dataloop.io"
arch=('x86_64')
license=('GPL3')
depends=()
optdepends=()
makedepends=()
conflicts=()
replaces=()
backup=()
install='dataloop-agent.install'
source=("https://download.dataloop.io/deb/pool/main/d/dataloop-agent/${pkgname}_${pkgver}-${pkgrel}_amd64.deb"
        "dataloop-agent.service")
sha512sums=('f3adf0f71994dd1432bcfa37090ef6b7d59969938abba8b4bbb3728b9919b2b520b8eebdd54ba28284b15552b1f25ee340879abcb922e204e4039737bab347e2'
            'cddcdbea636e40c67d8d396b477623cffd5219e3155422dc53196e9ede9736dde73ef7a9cac16ffa4d6cce924f533ed6618616673bf808656e8022342be01b16')

package() {
  tar -xf data.tar.gz -C "$pkgdir/"

  # get rid of the SysV
  rm -rf "$pkgdir/etc/init.d"
  rm -rf "$pkgdir/etc/default"

  # install systemd unit file
  install -Dm644 ../dataloop-agent.service "$pkgdir"/usr/lib/systemd/system/dataloop-agent.service

}

# vim:set ts=2 sw=2 et:
