# Maintainer: Ettore Chimenti <ek5.chimenti @ gmail.com>
pkgname="init-headphone"
pkgver="0.2.0"
pkgrel=1
epoch=
pkgdesc="Re-enables headphone jack after sleep/suspend resume on VIA VT1802"
arch=("any")
url="https://bugs.launchpad.net/ubuntu/+source/alsa-driver/+bug/1313904/"
license=('GPL')
groups=()
depends=("dmidecode" "python2-smbus" "python")
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=init-headphone.install
changelog=
source=("https://bugs.launchpad.net/ubuntu/+source/alsa-driver/+bug/1313904/+attachment/4361090/+files/${pkgname}_${pkgver}_all.deb"
        "init-headphone.service"  
        "init-headphone.install"
        )
noextract=()
md5sums=('37c830340c4ca077271a04b4436ea8fc'
         '8eaf6ff36bfe0927aec5677cb17fbbcc'
         'a47855a948f9684ea69db75f2cdd7398')
validpgpkeys=()

package() {

  tar -xf data.tar.xz -C $pkgdir

  mv $pkgdir/usr/{s,}bin
  rm -r $pkgdir/etc/init  

  mkdir -p  $pkgdir/etc/systemd/system
  cp init-headphone.service $pkgdir/etc/systemd/system
}


