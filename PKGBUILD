pkgname=apple-font-pack
pkgver=2026.08.07
pkgrel=1
pkgdesc="Apple fonts for RedBon"
arch=('x86_64')
license=('MIT')
options=('!strip')

package() {
  install -dm755 "${pkgdir}/usr/share/fonts/apple-font-pack"
  cp -r "${srcdir}/apple-font-pack/"* "${pkgdir}/usr/share/fonts/apple-font-pack/"
  find "${pkgdir}/usr/share/fonts/apple-font-pack" -type f -exec chmod 644 {} \;
}

post_install() {
  fc-cache -f
}
