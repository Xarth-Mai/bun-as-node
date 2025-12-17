# Maintainer: Xarth-Mai <g@lzzz.ink>
pkgname=bun-as-node
pkgver=1.0.0
pkgrel=1
pkgdesc="Force system to use Bun as Node.js and prevent Node.js installation"
arch=('any')
url="https://bun.sh"
license=('MIT')

depends=('bun')

provides=('nodejs' 'npm' 'npx')

conflicts=('nodejs' 'npm')

package() {
    mkdir -p "$pkgdir/usr/bin"
    ln -sf /usr/bin/bun "$pkgdir/usr/bin/node"
    ln -sf /usr/bin/bun "$pkgdir/usr/bin/nodejs"
    ln -sf /usr/bin/bun "$pkgdir/usr/bin/npm"
    ln -sf /usr/bin/bun "$pkgdir/usr/bin/npx"
    echo " > Linked: node, nodejs, npm, npx -> bun"
}