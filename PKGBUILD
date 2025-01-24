pkgname=avarice
pkgver=2.14
pkgrel=8
epoch=
pkgdesc="GDB debug server for AVR microcontrollers"
arch=('x86_64')
url=""
license=('GPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(git+https://github.com/avrf0/avarice.git)
noextract=()
md5sums=('SKIP')
validpgpkeys=()

prepare() {
	cd "${srcdir}/${pkgname}"
}

build() {
	cd "${srcdir}/${pkgname}"
	./Bootstrap
	./configure
	make all
}

check() {
	cd "${srcdir}/${pkgname}"
	make -k check
}

package() {
	cd "${srcdir}/${pkgname}"
	make DESTDIR="$pkgdir/" install
}
