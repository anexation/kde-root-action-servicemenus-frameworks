# Maintainer: anex <assassin.anex[@]gmail.com>

pkgname=kde-root-action-servicemenus-frameworks
pkgver=20141217
pkgrel=1
pkgdesc="Allows admin users to perform several root only actions from dolphin via kdesu/kdesudo"
arch=('any')
url="https://github.com/anexation/kde-root-action-servicemenus-frameworks"
license=('GPL')
depends=('dolphin-frameworks-git' 'kdialog-frameworks-git' 'ark-frameworks-git')
source=("${pkgbase}-${pkgver}-${pkgrel}.tar.gz::${url}/archive/${_git}.tar.gz")
md5sums=('SKIP')
10=10-rootactionsfolders.desktop
11=11-rootactionsfolders.desktop
rapl=rootactions-servicemenu.pl
raxml=root-servicemenu.xml

package() {
cp -r "${srcdir}/${pkgbase}-${_git}/10-rootactionsfolders.desktop" "${10}/usr/share/kservices5/ServiceMenus"
cp -r "${srcdir}/${pkgbase}-${_git}/11-rootactionsfolders.desktop" "${11}/usr/share/kservices5/ServiceMenus"
cp -r "${srcdir}/${pkgbase}-${_git}/rootactions-servicemenu.pl" "${rapl}/usr/bin"
cp -r "${srcdir}/${pkgbase}-${_git}/root-servicemenu.xml" "${raxml}/usr/share/apps/krusader"
find "${10}/usr/share/kservices5/ServiceMenus" -type d -exec chmod 755 '{}' \;
find "${11}/usr/share/kservices5/ServiceMenus" -type f -exec chmod 755 '{}' \;
find "${rapl}/usr/bin" -type d -exec chmod 777 '{}' \;
find "${raxml}/usr/share/apps/krusader" -type f -exec chmod 755 '{}' \;
}
