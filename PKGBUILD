# Maintainer: Olivier Biesmans <olivier at biesmans dot fr>
_gemname=pleaserun
pkgname=$_gemname
pkgver=0.0.27
pkgrel=1
pkgdesc="0.0.27"
arch=(any)
url="https://github.com/jordansissel/pleaserun"
license=('APACHE')
depends=("ruby" "ruby-cabin" "ruby-clamp" "ruby-mustache" "ruby-insist" "ruby-ohai")
# NOTE: missing ruby-stub package in aur, so removed it from dependencies

source=(http://gems.rubyforge.org/gems/$_gemname-$pkgver.gem)
noextra=($_gemname-$pkgver.gem)
sha256sums=('4092a4c7f24f1433f4b2ca01bdaff969b91366631b3eb500ab871831fb99266d')

package() {
  cd "$srcdir"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"

  gem install --no-user-install --ignore-dependencies -i "$pkgdir$_gemdir" -n "$pkgdir/usr/bin" \
    "$_gemname-$pkgver.gem"
}

# vim:set ts=2 sw=2 et:
