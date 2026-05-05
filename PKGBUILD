pkgname=panache-bin
pkgver=2.42.0
pkgrel=1
pkgdesc="A language server, formatter, and linter for Pandoc, Quarto, and R Markdown"
arch=('x86_64' 'aarch64')
url="https://github.com/jolars/panache"
license=('MIT')
depends=('gcc-libs')
provides=('panache')
conflicts=('panache')
options=(!strip)
source_x86_64=("panache-$pkgver-x86_64-unknown-linux-gnu.tar.gz::$url/releases/download/v$pkgver/panache-x86_64-unknown-linux-gnu.tar.gz")
source_aarch64=("panache-$pkgver-aarch64-unknown-linux-gnu.tar.gz::$url/releases/download/v$pkgver/panache-aarch64-unknown-linux-gnu.tar.gz")
sha256sums_x86_64=('7d742824aacb1a2c73c989278408a8f88dea414782de6aee6efecfb5e34090d8')
sha256sums_aarch64=('58960fb1042ac062fd562699859ee0d5b86c64fafea2c84688c9e15baae2a37e')

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
