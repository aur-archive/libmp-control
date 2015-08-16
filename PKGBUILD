pkgname=libmp-control
pkgver=148.18f2db7
pkgrel=1
pkgdesc="Library and Vala bindings to work with mpv slave mode"
arch=('i686' 'x86_64')
url="https://github.com/alphaos/build"
license=('GPL')
depends=('mpv')
makedepends=('vala' 'git')
source=(alphaos::git+https://github.com/alphaos/build)
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/alphaos
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd "$srcdir"/alphaos/def-scripts/03_extra/$pkgname/$pkgname
  make DESTDIR="$pkgdir/" install
}
