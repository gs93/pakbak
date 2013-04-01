# Maintainer: Giuliano Schneider <gs93@gmx.net>
pkgname=pakbak
pkgver=1.0.0
pkgrel=1
pkgdesc="Back up the local pacman database when it changes"
arch=('any')
license=('GPL')
depends=('bash' 'findutils' 'tar' 'systemd')
makedepends=()
source=("pakbak" "pakbak.conf" "pakbak.service" "pakbak.path")
install=pakbak.install
sha512sums=('004280bfbbc23a6550b455757df22c56d8e4535c70eecdf8bb2b2dbf7b45d2064b7afc07867fa727d52d968f25b2c9719866296b2eab4205bee4c6f856af1408'
        '0182765d961bc66fb694c6cf91df75d5599df7472e75eafffed4223710ddd2eb4d6fa47c6c3b374723f694046521bd3b1110f5801d612b10191f76c767913fe6'
        '4279dd18fbd3e24e41553dceeb9c82e16a5b5a37b40ef87f057aed25a4cfea2670a2e0927dc4b0fab7f726afb11b4f4a4313bf519f2cdcdbb0d6d8b8b8c117a2'
        '98165d85a7fadbe1010484ce1d7a8484483e9725cc70293bd3956b86851aebaaaf47e3cd49f88d2837fed0438ce67bbd1854f8a3100f0e81f6bb604a077c5341')
md5sums=('ce724c572c7447a8a378168a171dc771'
        'dec305832c4b00ae170c8a55f3b606f0'
        '3fd4e69a25cd7d6137f056f293bffe83'
        '87202867ffa029c89f27e3b164992b4a')

package() {
    cd "$srcdir"

    mkdir -p "$pkgdir/usr/lib/systemd/scripts"
    install -Dm755 pakbak "$pkgdir/usr/lib/systemd/scripts/pakbak"

    mkdir -p "$pkgdir/etc"
    install -Dm644 pakbak.conf "$pkgdir/etc/pakbak.conf"

    mkdir -p "$pkgdir/usr/lib/systemd/system"
    install -Dm644 pakbak.service "$pkgdir/usr/lib/systemd/system/pakbak.service"
    install -Dm644 pakbak.path "$pkgdir/usr/lib/systemd/system/pakbak.path"
}
