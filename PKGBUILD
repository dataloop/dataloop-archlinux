# Maintainer: Tom Ashley <tom.ashley[at]dataloop[dot]io>
pkgname=dataloop-agent
pkgver=1.4.5
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
sha512sums=('3a234a86c8072780a51daad025a1951bba07e24ecee6e4adabe01044a301d2f8079e4b1483047b0dc255b43d749f76fdb1e153a292e4b7ece9491414eb2b33b7'
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
