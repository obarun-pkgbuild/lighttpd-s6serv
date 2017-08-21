# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=lighttpd-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="lighttpd service for s6"
arch=(x86_64)
license=('beerware')
depends=('lighttpd' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('lighttpd.daemon.run.s6'
		'lighttpd.log.run.s6'
		'lighttpd.logd'
		'LICENSE')
md5sums=('b78e3d9ea8e146aa68185de3bbbab8e3'
         'ec6f04cf005f4c718f35ce5091dac288'
         'f3fbb3a7d0900001926da45905f8f463'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/lighttpd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/lighttpd/run"
	
	# log
	install -Dm 0755 "$srcdir/lighttpd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/lighttpd/log/run"
	install -Dm 0644 "$srcdir/lighttpd.logd" "$pkgdir/etc/s6-serv/log.d/lighttpd"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/lighttpd-s6serv/LICENSE"
}
