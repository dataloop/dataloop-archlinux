# Maintainer: Tom Ashley <tom.ashley[at]dataloop[dot]io>
pkgname=dataloop-agent
pkgver=1.1.20
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
        "dataloop-agent.service"
        )
md5sums=('e77e1f813f3bf97e11654bf40f2c3751'
         'bbb9a1da3f180e561473108707dbd58e'
        )

package() {
  tar -xf data.tar.gz -C "$pkgdir/"

  # get rid of the SysV
  rm -rf "$pkgdir/etc/init.d"
  rm -rf "$pkgdir/etc/default"

  # install systemd unit file
  install -Dm644 ../dataloop-agent.service "$pkgdir"/usr/lib/systemd/system/dataloop-agent.service

}
# vim:set ts=2 sw=2 et:
