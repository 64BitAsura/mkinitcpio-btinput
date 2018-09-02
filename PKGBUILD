# Author: Aline Freitas <aline@alinefreitas.com.br>
pkgname=mkinitcpio-btinput
pkgver=1.1
pkgrel=1
pkgdesc="This is a initcpio hook for bluetooth input devices. This is very useful if you have a bluetooth keyboard and use 'encrypt' hook"
url="https://github.com/irreleph4nt/mkinitcpio-btinput/"
arch=('x86_64' 'i686')
license=('GPLv2')
depends=('mkinitcpio' 'bluez')
makedepends=()
conflicts=()
replaces=()
backup=()
install=mkinitcpio-btinput.install
source=(install_btinput hook_btinput system.conf bluetooth.conf group 
passwd)
md5sums=('SKIP'
         'SKIP'
         'SKIP'
	 'SKIP'
         'SKIP'
         'SKIP')

package() {
  install -Dm644 install_btinput "${pkgdir}/usr/lib/initcpio/install/btinput"
  install -Dm644 hook_btinput "${pkgdir}/usr/lib/initcpio/hooks/btinput"
  install -Dm644 system.conf "${pkgdir}/usr/lib/initcpio/dbus/system.conf"
  install -Dm644 bluetooth.conf "${pkgdir}/usr/lib/initcpio/dbus/bluetooth.conf"
  install -Dm644 group "${pkgdir}/usr/lib/initcpio/dbus/group"
  install -Dm644 passwd	"${pkgdir}/usr/lib/initcpio/dbus/passwd"
}

# vim:set ts=2 sw=2 et:
