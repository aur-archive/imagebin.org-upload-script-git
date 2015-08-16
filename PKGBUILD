# Maintainer: Stephen Zhang <zsrkmyn@gmail.com>
pkgname=imagebin.org-upload-script-git
pkgver=0.6.0fe4143
pkgrel=1
pkgdesc="A script to upload images to imagebin.org"
arch=('any')
url="https://github.com/m13253/imagebin.org-upload-script"
license=('MIT')
depends=('python' 'python-requests')
makedepends=('git')
source=('git://github.com/m13253/imagebin.org-upload-script')
md5sums=(SKIP) #generate with 'makepkg -g'

_gitname="imagebin.org-upload-script"

pkgver() {
  cd $srcdir/$_gitname
  echo "0.$(git rev-list --count HEAD).$(git describe --always)"
}

package() {
  cd "$srcdir/$_gitname"
  mkdir -p $pkgdir/usr/bin/
  install -Dm655 pasteimg "$pkgdir/usr/bin/"
}

# vim:set ts=2 sw=2 et:
