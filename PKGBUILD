pkgname=apple-font-pack
pkgver=2026.09.01
pkgrel=1
pkgdesc="Apple fonts for RedBon with automatic Fontconfig defaults"
arch=('any')
license=('MIT')
depends=('fontconfig' 'ttf-fira-code')
options=('!strip')

package() {
  # 1. Install fonts with correct 644 permissions
  install -dm755 "${pkgdir}/usr/share/fonts/apple-font-pack"
  
  find "${srcdir}/apple-font-pack" -type f \( -name "*.otf" -o -name "*.ttf" \) \
    -exec install -Dm644 {} "${pkgdir}/usr/share/fonts/apple-font-pack/" \;

  # 2. Install global Fontconfig configuration
  install -Dm644 "${startdir}/99-apple-font-pack.conf" \
    "${pkgdir}/etc/fontconfig/conf.d/99-apple-font-pack.conf"
}
