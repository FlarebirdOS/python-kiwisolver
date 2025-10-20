pkgname=python-kiwisolver
pkgver=1.4.9
pkgrel=2
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
sha256sums=(6e55ef610b69f495fc4d322a153198f3e310615a5e1a63ef25635ea8cc3f2831)

build() {
    cd kiwi

    python3 -m build --wheel --no-isolation
}

package() {
    cd kiwi

    python3 -m installer -d ${pkgdir} dist/*.whl
}
