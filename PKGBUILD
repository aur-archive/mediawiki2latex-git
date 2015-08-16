# Mainainer: Pierre Neidhardt <ambrevar@gmail.com>

pkgname=mediawiki2latex-git
pkgver=v6.5
pkgrel=1
pkgdesc="MediaWiki To LaTeX converts MediaWiki markup to LaTeX and generates a PDF"
provides=(mediawiki2latex)
conflicts=(mediawiki2latex)
license=('GPL2')
arch=('i686' 'x86_64')
url="https://sourceforge.net/projects/wb2pdf/"
makedepends=('ghc'
    'haskell-hxt'
    'haskell-bytestring'
    'haskell-process'
    'haskell-temporary'
    'haskell-file-embed'
    'haskell-url>=2.1'
    'haskell-hxt-http>=9'
    'haskell-hxt>=8'
    'haskell-utf8-string>=0.3.6'
    'haskell-parsec>=2.1'
    'haskell-http>=4000'
    'haskell-split>=0.1.2.3'
    'haskell-containers>=0.3'
    'haskell-base>=4.1'
    'haskell-highlighting-kate>=0.5'
    'haskell-utility-ht>=0.0.5'
    'haskell-transformers>=0.2'
    'haskell-directory>=1.0'
    'haskell-blaze-html'
    'haskell-mtl'
    'haskell-network>=2.3.0.13')
depends=("texlive-bin"
    "texlive-core"
    "texlive-fontsextra"
    "texlive-latexextra")
source=(mediawiki2latex::git://git.code.sf.net/p/wb2pdf/git)
md5sums=('SKIP')

pkgver() {
    cd mediawiki2latex
    git describe --always | sed 's|-|.|g'
}

build() {
    cd mediawiki2latex
    make
}

package() {
    cd mediawiki2latex
    make DESTDIR="${pkgdir}" PREFIX=/usr install
}
