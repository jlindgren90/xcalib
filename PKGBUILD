# Maintainer: Santiago Torres-Arias <santiago@archlinux.org>
# Contributor: Vasya Novikov <vnn91@yandex.ru>
# Contributor: gato_lento
# Contributor: Yaroslav <proniyaroslav@mail.ru>
# Contributor: Frank Ickstadt (frank dot ickstadt at gmail dot com)
# Contributor: mOLOk

pkgname=xcalib
pkgver=0.10
pkgrel=3
pkgdesc="Load 'vcgt'-tag profiles to X-server on the calibration stage"
arch=('x86_64')
url="https://github.com/OpenICC/xcalib"
license=('GPL2' 'custom:postcardware')
depends=('libxxf86vm' 'libxrandr')

build() {
    cd ..
    make
}

package() {
    cd ..
    install -m755 -Dt "${pkgdir}/usr/bin" "xcalib"
    install -m644 -Dt "${pkgdir}/usr/share/man/man1/" "xcalib.1"
    install -m644 -Dt "${pkgdir}/usr/share/xcalib" *.icc
    install -m644 -Dt "${pkgdir}/usr/share/pixmaps/${pkgname}.ico" "icon.ico"

    # postcardware license stuff :)
    install -m644 -Dt "${pkgdir}/usr/share/licenses/xcalib/" "README.md"
}
