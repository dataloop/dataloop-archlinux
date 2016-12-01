# Maintainer: Tom Ashley <tom.ashley[at]dataloop[dot]io>
pkgname=dataloop-agent
pkgver=1.3.16
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
backup=('etc/dataloop/agent.yaml')
install='dataloop-agent.install'
source=("https://download.dataloop.io/deb/pool/main/d/dataloop-agent/${pkgname}_${pkgver}-${pkgrel}_amd64.deb"
        "dataloop-agent.service")
sha512sums=('dcda9ab8c73154ab1293ea38383dc7ab465505bac57afd84351a6f06d8641d5cf898e430725302c8cea971170df3fa19cd587fd5a3316ea1cd896eb90e6fb662'
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
