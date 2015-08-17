# Maintainer: Dustin Falgout <dustin@falgout.us>

pkgname=scangearmp-mg2200
pkgver=2.00
pkgrel=3
pkgdesc="Canon Scanner Driver For MG-2200"
arch=('i686' 'x86_64')
url="http://support-au.canon.com.au/contents/AU/EN/0100469601.html"
license=('unknown')
depends=('cnijfilter-common-mg2200')
makedepends=('rpmextract')
source=("http://gdlp01.c-wss.com/gds/6/0100004696/01/scangearmp-mg2200series-2.00-1-rpm.tar.gz")
md5sums=('4e2e3b80e578b5e7784b8c6471c2113f')

build() {
  if [ "${CARCH}" = 'x86_64' ]; then
    rpmfile=$(find "$srcdir" -name scangearmp-mg2200series-$pkgver*${CARCH}*.rpm)
  elif [ "${CARCH}" = 'i686' ]; then
    rpmfile=$(find "$srcdir" -name scangearmp-mg2200series-$pkgver*i386*.rpm)
  fi
 
}

package() {

	 cd $pkgdir
	rpmextract.sh $rpmfile

}
