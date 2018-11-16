

pkgname=bcachefs-tools-git
pkgver=392
pkgrel=1
pkgdesc="bcachefs filesystem utilities"
provides=('bcachefs-tools')
url="https://evilpiepirate.org/git/bcachefs-tools.git/"
arch=('x86_64')
license=('GPL2')

makedepends=("libscrypt-git")

source=("git+http://evilpiepirate.org/git/bcachefs-tools.git")
sha512sums=('SKIP')

pkgver() {
    cd bcachefs-tools

    echo $(git rev-list --count HEAD)
}

build() {
    cd bcachefs-tools

    make
}

package() {
    cd bcachefs-tools

    make DESTDIR="${pkgdir}/usr" ROOT_SBINDIR=/bin install
}