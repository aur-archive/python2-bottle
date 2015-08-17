# Contributor: Richard Murri <admin@richardmurri.com>
# Contributor: Farhad Shahbazi <farhad@enthusiasm.cc>
# Maintainer: Felix Kaiser <felix.kaiser@fxkr.net>

pkgname=python2-bottle
pkgver=0.11.4
pkgrel=1
pkgdesc="a fast and simple micro-framework for small web-applications"
arch=(any)
url="http://bottlepy.org"
license=('MIT')
depends=('python2')
options=(!emptydirs)
source=(http://pypi.python.org/packages/source/b/bottle/bottle-${pkgver}.tar.gz)
md5sums=('f767c340de0b7c9581917c48e609479b')

build() {
  cd "${srcdir}/bottle-${pkgver}"
  python2 setup.py install --root="${pkgdir}" --optimize=1

  # deal with the conflict with python-bottles version of /usr/bin/bottle.py
  mv "$pkgdir/usr/bin/bottle.py"{,2}
}
