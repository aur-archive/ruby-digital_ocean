# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=digital_ocean
pkgname=ruby-$_gemname
pkgver=1.5.0
pkgrel=2
pkgdesc='This gem wraps the DigitalOcean API documented at https://api.digitalocean.com/'
arch=(any)
url='https://github.com/rmoriz/digital_ocean'
license=(MIT)
depends=(ruby ruby-faraday ruby-faraday_middleware ruby-json ruby-hashie-2)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('b896f2f9e88bbc4a627704f7630b9fbe3c2d05ce')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
