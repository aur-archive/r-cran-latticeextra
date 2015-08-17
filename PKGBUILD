# Maintainer: Francois Garillot <francois[@]garillot.net>
pkgname=r-cran-latticeextra
pkgver=0.6_26
pkgrel=1
pkgdesc="Extra Graphical Utilities Based on Lattice"
url="http://cran.r-project.org/web/packages/latticeExtra/index.html"
license=('GPL (>= 2)')
arch=('i686' 'x86_64')
makedepends=('gcc' 'gcc-fortran')
depends=('r' 'r-cran-rcolorbrewer')
optdepends=('r-cran-deldir' 'r-cran-zoo' 'r-cran-mapproj' 'r-cran-maps' 'r-cran-tripack' 'r-cran-quantreg')
source=(http://cran.r-project.org/src/contrib/latticeExtra_0.6-26.tar.gz)
build() {
    mkdir -p ${pkgdir}/usr/lib/R/library
    cd ${srcdir}
    R CMD INSTALL latticeExtra -l ${pkgdir}/usr/lib/R/library
    for lic in "LICENSE" "LICENCE" "COPYING"; do
        if [ -f ${srcdir}/latticeExtra/${lic} ]; then
            install -Dm644 ${srcdir}/latticeExtra/${lic} ${pkgdir}/usr/share/licenses/r-cran-latticeextra/${lic}
        fi
    done
}
md5sums=('f17954ceb5333c1a9bd7fe3f175aac6c')
