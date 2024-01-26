# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Levi Zim <rsworktech@outlook.com>
pkgname=gparted-live-hd-bin
_pkgver=1.5.0-6
pkgver="${_pkgver/-/+}"
pkgrel=1
pkgdesc="gparted live installation in /boot (requires /boot partition supported by grub)"
arch=(x86_64)
url="https://gparted.org/livehd.php"
license=('GPL-2.0-or-later')
depends=('grub')
install=gparted-live-hd.install
source=("gparted-live.iso::https://sourceforge.net/projects/gparted/files/gparted-live-stable/$_pkgver/gparted-live-$_pkgver-amd64.iso"
        36_gparted-live-hd)
noextract=(gparted-live.iso)
sha256sums=('429fe13a3b6f3eb018afac8b0679ed8dd587bc2eb594b797efad2554119d7b27'
            'e186a17ee6cf6afdcce8436d53db81ac649e804ffc7faf749a0686cbbbefbdd9')


package() {
	install -Dvm644 gparted-live.iso -t "$pkgdir"/boot
	install -Dvm755 36_gparted-live-hd -t "$pkgdir"/etc/grub.d
}
