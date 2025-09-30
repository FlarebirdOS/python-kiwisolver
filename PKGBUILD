pkgname=python-kiwisolver
pkgver=1.4.7
pkgrel=1
pkgdesc="A fast implementation of the Cassowary constraint solver"
arch=('x86_64')
url="https://github.com/nucleic/kiwi"
license=('BSD-3-Clause')
depends=('python')
makedepends=(
    'git'
    'python-cppy'
    'python-setuptools-scm'
    'python-wheel'
    'python-build'
    'python-installer'
)
source=(git+ssh://git@github.com/nucleic/kiwi.git#tag=${pkgver})
sha256sums=(e6269bd66822e209f98aff87061dd020e25aa2d119db2f8be8f505fca14874c6)

build() {
    cd kiwi

    python3 -m build --wheel --no-isolation
}

package() {
    cd kiwi

    python3 -m installer -d ${pkgdir} dist/*.whl
}
