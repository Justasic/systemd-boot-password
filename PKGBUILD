# Maintainer: kitsunyan <kitsunyan@inbox.ru>

pkgname=systemd-boot-password-git
pkgver=1.0.237
pkgrel=1
pkgdesc='systemd-boot with password-protected editor'
arch=('i686' 'x86_64')
url="https://github.com/kitsunyan/$pkgname"
license=('LGPL2.1')
makedepends=('gnu-efi-libs' 'docbook-xsl')
optdepends=('sbsigntools: signing support')
source=("$pkgname::git+https://github.com/Justasic/systemd-boot-password.git")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  ./autogen.sh
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" install
}

