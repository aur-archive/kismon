# Maintainer: Max Roder <maxroder at web dot de>
# Contributor: Nathan Owe <ndowens.aur at gmail dot com>

pkgname=kismon
pkgver=0.6
pkgrel=2
pkgdesc="A PyGTK client that creates a map of a network"
arch=('any')
url="http://www.salecker.org/software/kismon/en"
license=('BSD')
depends=('pyclutter' 'pygtk' 'python2-simplejson' 'python-osmgpsmap' 'kismet')
source=("http://files.salecker.org/${pkgname}/${pkgname}-${pkgver}.tar.gz"
		"LICENSE")
sha256sums=('7ae6bf17d1806ad208d1ee31cd80a057baecc6dc49cc5bda4628e6a0a5751aa1'
            '688f54c468d21583c75d4c0ed8112f3bfc9dcb9f5418b6cdf3e0198d1e7e01c8')
build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  python2 setup.py build

}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  python2 setup.py install --root=${pkgdir}

  install -Dm644 ${srcdir}/LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE

}

# vim:set ts=2 sw=2 et:
