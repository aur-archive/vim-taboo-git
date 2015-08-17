# Contributor: Zsolt Udvari <udvzsolt gmail com>
pkgname=vim-taboo-git
_gitname=taboo.vim
pkgver=84.e2f1ea3
pkgrel=1
pkgdesc="Simple plugin for easily customize and rename tabs in vim"
arch=(any)
url="https://github.com/gcmt/taboo.vim"
license=('custom')
makedepends=(git)
depends=(vim)
install=vimdoc.install
groups=('vim-plugins')
source=(git://github.com/gcmt/taboo.vim.git)
md5sums=(SKIP)

pkgver() {
    cd $_gitname
    echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

build() {
    true
}

package() {
    cd $_gitname
    install -d ${pkgdir}/usr/share/vim/vimfiles/plugin
    install -d ${pkgdir}/usr/share/vim/vimfiles/doc
    install -d ${pkgdir}/usr/share/licenses/${pkgname}
    install -d ${pkgdir}/usr/share/doc/${pkgname}

    install -m644 plugin/taboo.vim ${pkgdir}/usr/share/vim/vimfiles/plugin
    install -m644 doc/taboo.txt ${pkgdir}/usr/share/vim/vimfiles/doc
    install -m644 LICENSE.txt ${pkgdir}/usr/share/licenses/${pkgname}
    install -m644 README.md ${pkgdir}/usr/share/doc/${pkgname}
}

