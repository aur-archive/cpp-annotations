pkgname=cpp-annotations
pkgver=10.1.0
pkgrel=1
pkgdesc="An extensive tutorial about the C++ programming language"
url="http://sourceforge.net/projects/cppannotations/"
arch=('i686' 'x86_64')
license=('GPLv3')
options=(zipman)
makedepends=('zip')
source=($pkgname-$pkgver-$pkgrel.html.zip::http://sourceforge.net/projects/cppannotations/files/cppannotations/$pkgver/cplusplus.html.zip
        $pkgname-$pkgver-$pkgrel.txt.zip::http://sourceforge.net/projects/cppannotations/files/cppannotations/$pkgver/cplusplus.txt.zip)

build() {
   true
}

pkgver()
{
  cd $srcdir/cppannotations/html
  grep -i '<title>' cplusplus.html | egrep  -o '[0-9.]*'
}

package() {
  cd $srcdir/cppannotations
#  install -m644 -D COPYING $pkgdir/usr/share/licenses/$pkgname/LICENSE
#  install -m644 -D README $pkgdir/usr/share/doc/$pkgname/README
  dest=$pkgdir/usr/share/doc/$pkgname
  mkdir -p "$dest"
  cp -r txt html "$dest"
  chmod a=rX,u=rwX "$dest"
}


md5sums=('c90b3fc435c29c82c77315d6bde05110'
         'f629b6a7a59b7a68247ca96438207da7')
