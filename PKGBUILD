pkgname=port-forward-git
gitname=port-forward
pkgver=v0.1.0.r2.gf9df791
pkgver() {
  cd "$gitname"
  git describe --long | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}
pkgrel=1
pkgdesc="Simple iptables frontend for portforwarding"
arch=('any')
url="https://github.com/TkkrLab/port-forward"
license=('GPL3')
depends=('iptables')
source=("git+https://github.com/TkkrLab/port-forward.git")
backup=('etc/port-forward.conf')
md5sums=('SKIP')
package() {
	install -d "$pkgdir/usr/sbin/"
	install -d "$pkgdir/usr/lib/systemd/system/"
	install -d "$pkgdir/etc/"
	install -m755 "$gitname/src/usr/local/sbin/port-forward" "$pkgdir/usr/sbin/port-forward"
	install -m644 "$gitname/src/usr/lib/systemd/system/port-forward.service" "$pkgdir/usr/lib/systemd/system/port-forward.service"
	install -m644 "$gitname/src/etc/port-forward.conf" "$pkgdir/etc/port-forward.conf"
}
