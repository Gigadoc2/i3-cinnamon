# Maintainer: Fabian Pack <gigadoc2@revreso.de>
# original Maintainer: Klaas Boesche <aurkagebe@gmail.com>
# Contributor: Alexandre Isoard <alexandre.isoard@gmail.com>
pkgname=i3-cinnamon
_pkgname=i3
pkgver=0.3
pkgrel=1
pkgdesc="Run i3 with cinnamon-session and cinnamon-settings-daemon"
url="https://github.com/Gigadoc2/i3-cinnamon"
arch=('any')
license=('GPL')
depends=("i3-wm>=4.0" "desktop-file-utils" "cinnamon-desktop" "cinnamon-screensaver" "polkit-gnome")

install=$pkgname.install
source=("$pkgname-xsession.desktop" "$pkgname" "$pkgname-app.desktop" "$pkgname.session" "cinnamon-session-$_pkgname")
md5sums=('b8f975696b7a7421f7f517018115e9a2'
         '0fb6c682b44e464ba5cd569e31694aba'
         'c69924f5975d9cc15fe04e68dd7f7195'
         '775ade4b8e1dcb5a855eed102007e9cf'
         '9c9077b4819c331ccecdebb498c5e7c6')

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

  msg "Install cinnamon-session-$_pkgname in /usr/bin"
  install -D -m 755 "$srcdir/cinnamon-session-$_pkgname" \
    "$pkgdir/usr/bin/cinnamon-session-$_pkgname"
}

# vim:set ts=2 sw=2 et:
