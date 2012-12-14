# Maintainer: Hyacinthe Cartiaux <hyacinthe.cartiaux@free.fr>

pkgname=firefox-tmpfs-daemon
pkgver=0.5
pkgrel=1
pkgdesc="Sync all ~/.mozilla directories to tmpfs at boot and stop time"
arch=(any)
url=https://bbs.archlinux.org/viewtopic.php?id=118576
license=('GPL')
depends=('firefox' 'rsync')
conflicts=('firefox-sync')
source=(  rc.firefox-tmpfs
          confd.firefox-tmpfs
          firefox-tmpfs.service )
md5sums=( 9b4e33f456dacee8de4e989938a3c08b
          fa5d47bc7bfa10b58212aa66c39fd960
          d40952135e263729177cc22020ae1d15 )
install=$pkgname.install
backup=(etc/conf.d/firefox-tmpfs)

package() {
  install -m 755 -D $srcdir/rc.firefox-tmpfs      $pkgdir/etc/rc.d/firefox-tmpfs
  install -m 644 -D $srcdir/confd.firefox-tmpfs   $pkgdir/etc/conf.d/firefox-tmpfs
  install -m 644 -D $srcdir/firefox-tmpfs.service $pkgdir/usr/lib/systemd/system/firefox-tmpfs.service
}

# vim:set ts=2 sw=2 et:
