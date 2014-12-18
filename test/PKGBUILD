# Maintainer: anex <assassin.anex[@]gmail.com>

pkgname=kde-root-action-servicemenus-frameworks
pkgver=20141217
pkgrel=1
pkgdesc="Allows admin users to perform several root only actions from dolphin via kdesu/kdesudo"
arch=('any')
url="https://github.com/anexation/kde-root-action-servicemenus-frameworks"
license=('GPL')
makedepends=('git')
depends=('dolphin-frameworks-git' 'kdialog-frameworks-git' 'ark-frameworks-git')
optdepends=("krusader-git")
source=("git+https://github.com/anexation/kde-root-action-servicemenus-frameworks.git")
md5sums=('SKIP')

package() {
mkdir -p "/usr/share/apps/krusader"
cp -a --no-preserve=ownership "${srcdir}/kde-root-action-servicemenus-frameworks/10-rootactionsfolders.desktop" "/usr/share/kservices5/ServiceMenus"
cp -a --no-preserve=ownership "${srcdir}/kde-root-action-servicemenus-frameworks/11-rootactionsfiles.desktop" "/usr/share/kservices5/ServiceMenus"
cp -a --no-preserve=ownership "${srcdir}/kde-root-action-servicemenus-frameworks/rootactions-servicemenu.pl" "/usr/bin"
cp -a --no-preserve=ownership "${srcdir}/kde-root-action-servicemenus-frameworks/root-servicemenu.xml" "/usr/share/apps/krusader"

}
