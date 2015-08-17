# Contributor:  Ben Alex <ben.alex@acegi.com.au>

pkgname=nxvalidate
pkgver=1.0.4
pkgrel=1
pkgdesc="Validates Nanex NxCore tape files"
arch=('x86_64')
url="http://github.com/benalexau/nxvalidate"
license=('APACHE')
depends=('bash' 'libnx' 'glibc')
makedepends=('git' 'make' 'gcc')
source=("nxgit"::'git+http://github.com/benalexau/nxvalidate.git#tag=v1.0.4')
md5sums=('SKIP')

build() {
	cd "$srcdir/nxgit"
        make
}

package() {
	cd "$srcdir/nxgit"
	install -Dm755 nxvalidate-dir "$pkgdir/usr/bin/nxvalidate-dir"
	install -Dm755 nxvalidate     "$pkgdir/usr/bin/nxvalidate"
}
