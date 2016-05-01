# Maintainer: Tom Ashley <tom.ashley[at]dataloop[dot]io>
pkgname=dataloop-agent
pkgver=1.1.35
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
sha512sums=('0a2fbccecca71a81c14222035eb04fc5f5e5204590b1f632ad657f5aa978246049104f1c7667066ce56290697cb2bbd849b5f0b2a53fbc89e495b6b90864d65b'
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
