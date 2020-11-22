pkgname=alsa-ucm-beryllium
pkgver=0.1
pkgrel=1
pkgdesc="UCM files for Xiaomi Pocophone F1"
arch=(any)
url="https://github.com/jld3103/alsa-ucm-beryllium"
license=('MIT')
depends=(alsa-ucm-conf)
source=("git+https://gitlab.com/sdm845-mainline/alsa-ucm-conf")
md5sums=('SKIP')

package() {
    for file in \
        "codecs/tas2559/DefaultDisableSeq.conf" \
        "codecs/tas2559/DefaultEnableSeq.conf" \
        "codecs/tas2559/EarpieceEnableSeq.conf" \
        "codecs/tas2559/SpeakersEnableSeq.conf" \
        "xiaomiberyllium/HiFi.conf" \
        "xiaomiberyllium/xiaomiberyllium.conf"; do
	    install -D -m644 "$srcdir"/alsa-ucm-conf/ucm2/"$file" \
		    "$pkgdir"/usr/share/alsa/ucm2/"$file"
    done
}
