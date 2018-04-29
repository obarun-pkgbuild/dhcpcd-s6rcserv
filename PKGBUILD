# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhcpcd-s6rcserv
pkgver=0.2
pkgrel=1
pkgdesc="dhcpcd service for"
arch=(x86_64)
license=('beerware')
depends=('dhcpcd' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dhcpcd.longrun.dependencies'
		'dhcpcd.longrun.finish'
		'dhcpcd.longrun.pipeline-name'
		'dhcpcd.longrun.producer-for'
		'dhcpcd.longrun.run'	
		'dhcpcd.longrun.type'		
		
		'dhcpcd.log.consumer-for'
		'dhcpcd.log.dependencies'
		'dhcpcd.log.run'
		'dhcpcd.log.type'
		
		'bundle.dhcpcd.contents'
		'bundle.dhcpcd.type'
		'dhcpcd.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '8a1fea4ffecc2dfa29f0022180309d8b'
         'bb5b1e51fc7ebdc9517d634d95d378cb'
         '30010e479e036f3f06377fddca5eb50c'
         '8c7539c0add42dac34c55781a706ada0'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '69ff8fed520cc77af03efa7831c8131c'
         '68b329da9893e34099c7d8ad5cb9c940'
         '326a5bda351a8abc6b63c702a5dae874'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'a9a22f206735601260c8fb99cf8742f1'
         '71abe97e2554d37f1d12c5bf4945297f'
         'ac0f8643ca680fd9ead19a2a351d2cf5'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dhcpcd need a maj at dhcpcd e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dhcpcd.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhcpcd/contents"
	install -Dm 0644 "$srcdir/bundle.dhcpcd.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhcpcd/type"
	
	# longrun
	install -Dm 0644 "$srcdir/dhcpcd.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/dependencies"
	install -Dm 0644 "$srcdir/dhcpcd.longrun.finish" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/finish"
	install -Dm 0644 "$srcdir/dhcpcd.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/dhcpcd.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/producer-for"
	install -Dm 0644 "$srcdir/dhcpcd.longrun.run" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/run"
	install -Dm 0644 "$srcdir/dhcpcd.longrun.type" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/dhcpcd.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/consumer-for"
	install -Dm 0644 "$srcdir/dhcpcd.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/dependencies"
	install -Dm 0644 "$srcdir/dhcpcd.log.run" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/run"
	install -Dm 0644 "$srcdir/dhcpcd.log.type" "$pkgdir/etc/s6-serv/available/rc/dhcpcd-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/dhcpcd.logd" "$pkgdir/etc/s6-serv/log.d/dhcpcd-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhcpcd-s6rcserv/LICENSE"
}
