# Maintainer: aps42 <arch@andre-sterba.de>
pkgname=containerlab-bin
pkgver=0.67.0
pkgrel=1
pkgdesc='containerlab enables container-based networking labs'
arch=('x86_64')
provides=(containerlab)
url='https://github.com/srl-labs/containerlab'
license=('BSD')

source=("${pkgname/-bin/}-${pkgver}.tar.gz::https://github.com/srl-labs/containerlab/releases/download/v${pkgver}/containerlab_${pkgver}_Linux_amd64.tar.gz")

sha256sums=('450f3b78569ee96763998f8e92934169e14a42a53b7b807b968cb97346f7975e')

package() {
  install -Dm755 ${pkgname/-bin/} "$pkgdir"/usr/bin/${pkgname/-bin/}

  install -d "${pkgdir}/etc/${pkgname/-bin/}/lab-examples"

  cp -r "${srcdir}/lab-examples/"* "$pkgdir/etc/${pkgname/-bin/}/lab-examples"
}

