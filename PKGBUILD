#Maintainer: Andrew Webley <unsuspectinghero@gmail.com>
pkgname=grub2-theme-archlinuxinstall
pkgver="0.1"
pkgrel="1"
pkgdesc="The bootloader theme from the Archlinux install image ported to Grub2"
url="https://github.com/ArchFwin/grub2-theme-archlinuxinstall"
arch=('any')
license=('GPL v3')
depends=('grub-bios')
makedepends=('git')
source=()
_gitroot="https://github.com/ArchFwin/grub2-theme-archlinuxinstall.git"
_gitname="grub2-theme-archlinuxinstall"

build() {
	cd "${srcdir}"
	msg "Connecting to GIT server...."
	
	if [ -d $_gitname ] ; then
		cd $_gitname && git pull origin
		msg "The local files are updated."
	else
		git clone -b master $_gitroot $_gitname
	fi
	
	msg "GIT checkout done or server timeout"

	if [ -d "${srcdir}/${_gitname}-build" ]
	then
		rm -rf "${srcdir}/${_gitname}-build"
	fi