# Maintainer: Fabian Pack <gigadoc2@revreso.de>
# original Maintainer: Klaas Boesche <aurkagebe@gmail.com>
# Contributor: Alexandre Isoard <alexandre.isoard@gmail.com>
pkgname=i3-cinnamon
_pkgname=i3
pkgver=0.1
pkgrel=1
pkgdesc="Run i3 with cinnamon-session and cinnamon-settings-daemon"
url="https://github.com/Gigadoc2/i3-cinnamon"
arch=('any')
license=('GPL')
depends=("i3-wm>=4.0" "desktop-file-utils" "cinnamon-desktop")

install=$pkgname.install
source=("$pkgname-xsession.desktop" "$pkgname" "$pkgname-app.desktop" "$pkgname.session")
md5sums=('8d98cff29a6dc097bfd5fb021d9244be'
         '0fb6c682b44e464ba5cd569e31694aba'
         'c69924f5975d9cc15fe04e68dd7f7195'
         'c37e6b483b157951ff8e5a0543b38969')

package() {
  msg "Install $pkgname in xsessions"
  install -D -m 644 "$srcdir/$pkgname-xsession.desktop" \
    "$pkgdir/usr/share/xsessions/$pkgname.desktop"

  msg "Install $pkgname in cinnamon-session/sessions"
  install -D -m 644 "$srcdir/$pkgname.session" \
    "$pkgdir/usr/share/cinnamon-session/sessions/$pkgname.session"

  msg "Install $pkgname in /ush/share/applications"
  install -D -m 644 "$srcdir/$pkgname-app.desktop" \
    "$pkgdir/usr/share/applications/$pkgname.desktop"

  msg "Install $pkgname in /usr/bin"
  install -D -m 755 "$srcdir/$pkgname" \
    "$pkgdir/usr/bin/$pkgname"
}

# vim:set ts=2 sw=2 et:
