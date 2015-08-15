# Maintainer: M0Rf30

pkgname=fretsonfirex
pkgver=3.121
pkgrel=2
pkgdesc="Highly improved version of Frets on Fire"
url="http://code.google.com/p/fofix"
arch=(any)
license=('GPL')
install=${pkgname}.install
groups=('games')
depends=('python2' 'python2-pygame' 'python2-opengl' 'python2-pillow' 'pyogg' 'pyvorbis' 'python2-pysqlite' 'libffi' 'python2-numpy')
makedepends=('git')
replaces=('fofix')
source=("fretsonfirex::git+https://github.com/M0Rf30/fofix-arch-fork.git" 
	'fretsonfirex.desktop' 
	'fretsonfirex.png'
	'fretsonfirex.sh')



package() {
  cd fretsonfirex
  install -d $pkgdir/usr/
  install -d $pkgdir/usr/share/
  install -d $pkgdir/usr/share/applications/
  install -d $pkgdir/usr/share/pixmaps/
  install -d $pkgdir/usr/bin/
  install -d $pkgdir/opt/fretsonfirex
  cp ../fretsonfirex.desktop ${pkgdir}/usr/share/applications/
  cp ../fretsonfirex.png ${pkgdir}/usr/share/pixmaps/
  cp -r {src,data,doc,svg} $pkgdir/opt/fretsonfirex/
  cp ../fretsonfirex.sh $pkgdir/usr/bin/fretsonfirex
  chmod +x $pkgdir/usr/bin/fretsonfirex
  chmod -R 777 $pkgdir/opt/fretsonfirex
}

pkgver() {
  cd fretsonfirex
  echo $(git tag)
}

md5sums=('SKIP'
         '0a4a9b64141c1215a06430319631c475'
         'f886a7fdfa7592b50aa9f62901910e03'
         'b3c01e519d65bbfa4bdc3fb93f2db965')
