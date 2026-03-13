pkgname=panache-bin
pkgver=2.20.0
pkgrel=1
pkgdesc="A language server, formatter, and linter for Pandoc, Quarto, and R Markdown"
arch=('x86_64' 'aarch64')
url="https://github.com/jolars/panache"
license=('MIT')
depends=('gcc-libs')
provides=('panache')
conflicts=('panache')
source_x86_64=("$url/releases/download/v$pkgver/panache-x86_64-unknown-linux-gnu.tar.gz")
source_aarch64=("$url/releases/download/v$pkgver/panache-aarch64-unknown-linux-gnu.tar.gz")
sha256sums_x86_64=('aa6e43016a40dd2adc31e3af3d5e235833466137c59276ac6f5c4930dc9806c3')
sha256sums_aarch64=('26b2f2253c8e40997ac201f8a11da3d1a8ca4fa794477460e24a070f327df621')

package() {
    # Binary
    install -Dm755 panache "$pkgdir/usr/bin/panache"

    # Man pages
    install -Dm644 man/*.1 -t "$pkgdir/usr/share/man/man1/"

    # Shell completions
    install -Dm644 completions/panache.bash "$pkgdir/usr/share/bash-completion/completions/panache"
    install -Dm644 completions/panache.fish "$pkgdir/usr/share/fish/vendor_completions.d/panache.fish"
    install -Dm644 completions/_panache "$pkgdir/usr/share/zsh/site-functions/_panache"

    # License
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
