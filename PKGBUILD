# Maintainer: PwnWriter < hey@pwnwriter.xyz >

pkgname=metis-skel
pkgver=1.0
pkgrel=1
pkgdesc="Skeleton Configurations for METIS Linux"
url="https://github.com/metis-os/metis-skel"
arch=('x86_64')
license=('MIT')
makedepends=('git')
depends=('zsh' 'python3' 'xorg-server' 'xorg-xinit' 'xwallpaper' 'fzf' 'doas')
conflicts=('SKIP')
provides=("${pkgname}")
options=(!strip !emptydirs)
install="${pkgname}.install"

prepare() {
	cp -af ../source/. ${srcdir}
}

package() {

        local _config=${pkgdir}/etc/skel/
	mkdir -p "$_config"

        cp -r ${srcdir}/xprofile       "$_config/.xprofile"
        cp -r ${srcdir}/zprofile       "$_config/.zprofile"
        cp -r ${srcdir}/config         "$_config/.config"
        cp -r ${srcdir}/cache          "$_config/.cache"
        cp -r ${srcdir}/local          "$_config/.local"
}

