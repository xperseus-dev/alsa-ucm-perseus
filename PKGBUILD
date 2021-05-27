pkgname=alsa-ucm-conf
pkgver=1.2.4
pkgrel=1
_commit=9e0051807472822bc4090a2d03ab5dacd7787ab8
pkgdesc="ALSA Use Case Manager configuration (and topologies) with Xiaomi Pocophone F1 configs"
arch=(any)
url="https://gitlab.com/sdm845-mainline/alsa-ucm-conf"
license=('BSD')
source=("git+https://gitlab.com/sdm845-mainline/alsa-ucm-conf.git/#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd alsa-ucm-conf
    find ucm2 -type f -iname "*.conf" -exec install -vDm 644 {} "${pkgdir}/usr/share/alsa/"{} \;
    find ucm2 -type l -iname "*.conf" -exec cp -dv {} "${pkgdir}/usr/share/alsa/"{} \;
    install -vDm 644 LICENSE -t "$pkgdir/usr/share/licenses/$pkgname"
    install -vDm 644 README.md -t "$pkgdir/usr/share/doc/$pkgname"
    install -vDm 644 ucm2/README.md -t "$pkgdir/usr/share/doc/$pkgname/ucm2"
}
