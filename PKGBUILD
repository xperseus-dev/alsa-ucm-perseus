pkgname=alsa-ucm-conf
pkgver=1.2.4
pkgrel=1
_commit=43a2e461c40fc1c1ef90d21c6d5aa1934ca2e82e
pkgdesc="ALSA Use Case Manager configuration (and topologies) with Xiaomi Mi MIX 3 configs"
arch=(any)
url="https://gitlab.com/xperseus/alsa-ucm-conf"
license=('BSD')
source=("git+https://gitlab.com/xperseus/alsa-ucm-conf.git/#commit=$_commit")
sha256sums=('SKIP')

package() {
    cd alsa-ucm-conf
    find ucm2 -type f -iname "*.conf" -exec install -vDm 644 {} "${pkgdir}/usr/share/alsa/"{} \;
    find ucm2 -type l -iname "*.conf" -exec cp -dv {} "${pkgdir}/usr/share/alsa/"{} \;
    install -vDm 644 LICENSE -t "$pkgdir/usr/share/licenses/$pkgname"
    install -vDm 644 README.md -t "$pkgdir/usr/share/doc/$pkgname"
    install -vDm 644 ucm2/README.md -t "$pkgdir/usr/share/doc/$pkgname/ucm2"
}
