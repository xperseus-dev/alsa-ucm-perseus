pkgname=alsa-ucm-beryllium
pkgver=0.2
pkgrel=1
_commit=9fc68c86
pkgdesc="UCM files for Xiaomi Pocophone F1"
arch=(any)
url="https://github.com/jld3103/alsa-ucm-beryllium"
license=('MIT')
depends=(alsa-ucm-conf)
source=("git+https://gitlab.com/sdm845-mainline/alsa-ucm-conf.git/#commit=$_commit")
md5sums=('SKIP')

package() {
    for file in \
        "Qualcomm/sdm845/HiFi.conf" \
        "Qualcomm/sdm845/sdm845.conf"; do
	    install -D -m644 "$srcdir"/alsa-ucm-conf/ucm2/"$file" \
		    "$pkgdir"/usr/share/alsa/ucm2/"$file"
    done
}
