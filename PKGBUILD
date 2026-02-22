pkgname=kwin-blur-reminder
pkgver=1.1.1
pkgrel=1
pkgdesc="Pacman hook + desktop notification reminding to rebuild KWin blur effect after KWin updates"
arch=('any')
url="https://localhost/"
license=('MIT')
depends=('bash' 'systemd' 'libnotify')
source=(
  "kwin-blur-reminder"
  "kwin-blur-reminder.hook"
)
sha256sums=('SKIP' 'SKIP')

package() {
  # script
  install -Dm755 "$srcdir/kwin-blur-reminder" "$pkgdir/usr/bin/kwin-blur-reminder"

  # pacman hook (libalpm hook dir for packaged hooks)
  install -Dm644 "$srcdir/kwin-blur-reminder.hook" \
    "$pkgdir/usr/share/libalpm/hooks/kwin-blur-reminder.hook"
}
