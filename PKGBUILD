# Maintainer : TimorLee

pkgname=gog-halfway
pkgver=1.4.0.6
pkgrel=1
pkgdesc="Halfway is a turn-based strategy RPG taking place a few hundred years into the future. GOG linux game package required"
arch=("i686" "x86_64")
url="http://www.gog.com/game/halfway"
license=("custom")
groups=("games")
source=("gog_halfway_${pkgver}.tar.gz" "gog-halfway")
md5sums=('cb3e1b6095586d23dbc4628157c40141'
         'bdfffa8b83305d87eba2e02f0d535afa')
depends=(libgl libx11 libxext desktop-file-utils)
#options=('!strip')
PKGEXT=.pkg.tar

package() {
  mkdir -p "${pkgdir}"/opt/gog/halfway
  cp -r "${srcdir}"/Halfway/* "${pkgdir}"/opt/gog/halfway
  install -Dm644 "${srcdir}"/Halfway/support/gog-halfway-primary.desktop "${pkgdir}"/usr/share/applications/gog-halfway.desktop
  install -Dm644 "${srcdir}"/Halfway/support/gog-halfway.png "${pkgdir}"/usr/share/pixmaps/gog-halfway.png
  install -Dm644 "${srcdir}"/Halfway/docs/End\ User\ License\ Agreement.txt "${pkgdir}"/usr/share/licenses/$pkgname/LICENSE
  install -Dm755 "${srcdir}/gog-halfway" "${pkgdir}/usr/bin/gog-halfway"
  chmod -R 777 "${pkgdir}"/opt/gog/halfway/
}
