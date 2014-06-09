# Maintainer: Stefaan Michielsen <stefaan@easics.be>
pkgname=('nvc-git')
pkgbase=BASE
pkgver=1
pkgrel=1
epoch=
pkgdesc=""
arch=('x86-64', 'x86')
url=""
license=('unknown')
groups=()
depends=()
makedepends=()
checkdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('nvc::git+https://github.com/nickg/nvc.git')
noextract=()
md5sums=()

#prepare() {
#	cd "$srcdir/$pkgname-$pkgver"
#	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
#}

build() {
	cd "$srcdir/$pkgbase-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$srcdir/$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
