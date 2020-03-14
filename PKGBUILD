pkgname=onedrive
pkgver=2.3.13
pkgrel=1
pkgdesc="Free OneDrive client written in D - abraunegg's fork. Follows the releases on https://github.com/abraunegg/onedrive/releases"
arch=('x86_64')
url="https://github.com/abraunegg/onedrive"
license=('GPL')
source=("https://github.com/abraunegg/onedrive/archive/v$pkgver.tar.gz")
depends=('curl' 'libnotify' 'sqlite' 'liblphobos')
makedepends=('dmd')

build() {
	cd "$pkgname-$pkgver"
        ./configure --sysconfdir=/etc --prefix=/usr --enable-notifications --enable-completions
        make
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR=$pkgdir PREFIX=/usr install
}
md5sums=('d36da03e2cdddf747be93c14baa066d6')
