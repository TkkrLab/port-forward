pkgname=port-forward
pkgver=1
pkgrel=1
pkgdesc="Simple iptables frontend for portforwarding"
arch=('any')
url="https://github.com/TkkrLab/port-forward"
license=('GPL3')
depends=('iptables')
source=("git+https://github.com/TkkrLab/port-forward.git")
md5sums=('SKIP')
package() {
	install -d "$pkgdir/usr/sbin/"
	install -d "$pkgdir/usr/lib/systemd/system/"
	install -d "$pkgdir/etc/"
	install -m755 "$pkgname/src/usr/local/sbin/port-forward" "$pkgdir/usr/sbin/port-forward"
	install -m644 "$pkgname/src/usr/lib/systemd/system/port-forward.service" "$pkgdir/usr/lib/systemd/system/port-forward.service"
	install -m644 "$pkgname/src/etc/port-forward.conf" "$pkgdir/etc/port-forward.conf"

}
