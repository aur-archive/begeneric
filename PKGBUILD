#Contributor: sxe <sxxe@gmx.de>

pkgname=begeneric
_realname=generic_animations-kwin-fx
pkgver=0.7b
pkgrel=1
pkgdesc="A generic animation effect for kwin."
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/Generic+Animations+%28BeGeneric+%3B-%29?content=145674"
depends=('kdebase-workspace>=4.3.0')
makedepends=('cmake' 'automoc4' 'gcc')
source=("http://kde-look.org/CONTENT/content-files/145674-${_realname}-${pkgver}.txz")
license=('GPL')

build() 

{
        cd $srcdir/${_realname}
        cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` -DCMAKE_BUILD_TYPE=Release .
        make || return 1
        make DESTDIR=$pkgdir install
	kbuildsycoca4
}

md5sums=('ed076c90f17f784e7c79806e78bd77a2')
