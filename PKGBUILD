# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhcpcd-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="dhcpcd service for s6"
arch=(x86_64)
license=('beerware')
depends=('dhcpcd' 's6' 's6-rc' 's6-boot')
conflicts=()
install=dhcpcd-s6rcserv.install
source=('dhcpcd.daemon.dependencies.s6'
		'dhcpcd.daemon.finish.s6'
		'dhcpcd.daemon.pipeline-name.s6'
		'dhcpcd.daemon.producer-for.s6'
		'dhcpcd.daemon.run.s6'	
		'dhcpcd.daemon.type.s6'		
		
		'dhcpcd.log.consumer-for.s6'
		'dhcpcd.log.dependencies.s6'
		'dhcpcd.log.run.s6'
		'dhcpcd.log.type.s6'
		
		'bundle.dhcpcd.contents.s6'
		'bundle.dhcpcd.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '8a1fea4ffecc2dfa29f0022180309d8b'
         'bb5b1e51fc7ebdc9517d634d95d378cb'
         '30010e479e036f3f06377fddca5eb50c'
         'bf803887425236d4f60b338444c554d7'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '83355bbdea29ac2de0a42c3a6f18fffe'
         '68b329da9893e34099c7d8ad5cb9c940'
         '326a5bda351a8abc6b63c702a5dae874'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '8598ba1c8749792dac59cba9f6c551d4'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dhcpcd need a maj at dhcpcd e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dhcpcd.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhcpcd/contents"
	install -Dm 0644 "$srcdir/bundle.dhcpcd.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhcpcd/type"
	
	# daemon
	install -Dm 0644 "$srcdir/dhcpcd.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/dependencies"
	install -Dm 0644 "$srcdir/dhcpcd.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/finish"
	install -Dm 0644 "$srcdir/dhcpcd.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/dhcpcd.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/producer-for"
	install -Dm 0644 "$srcdir/dhcpcd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/run"
	install -Dm 0644 "$srcdir/dhcpcd.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/dhcpcd.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/consumer-for"
	install -Dm 0644 "$srcdir/dhcpcd.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/dependencies"
	install -Dm 0644 "$srcdir/dhcpcd.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/run"
	install -Dm 0644 "$srcdir/dhcpcd.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhcpcd-s6rcserv/LICENSE"
}
