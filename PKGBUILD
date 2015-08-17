# Maintainer: Federico Rampazzo < frampone at gmail >

pkgname=the-league-of-moveable-type-fonts
pkgver=20130713
pkgrel=1
pkgdesc='Fonts collection by The League of Moveable Type'
arch=('i686' 'x86_64')
url='http://www.theleagueofmoveabletype.com/'
license=('custom:OFL')
makedepends=('git')
install='the-league-of-moveable-type-fonts.install'

build() {
  cd "$srcdir"  
  msg "Getting the list of available fonts...."

  repos=`wget --quiet -O - https://github.com/theleagueof | grep -oP '(?<=href=")[^"]*(?=")' | grep -oP '(?<=/theleagueof/)[^\/]*(?=/network)'`
  for i in $repos; do
    _gitroot="git://github.com/theleagueof/$i.git"
    _gitname=$i
    
    msg "Downloading $i...."
    
    msg "Connecting to GIT server...."

    if [[ -d "$_gitname" ]]; then
      cd "$_gitname" && git pull origin
      msg "The local files are updated."
      cd ..
    else
      git clone "$_gitroot" "$_gitname"
    fi
    
    msg "GIT checkout done or server timeout"
  done
}

package() {

  install -d "$pkgdir/usr/share/fonts/theleagueofmoveabletype"

  install -Dm644 "$srcdir/blackout/Blackout Midnight.ttf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/blackout/Blackout Sunrise.ttf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/blackout/Blackout Two AM.ttf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/chunk/Chunk.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/fanwood/Fanwood Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/fanwood/Fanwood Text Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/fanwood/Fanwood Text.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/fanwood/Fanwood.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/goudy-bookletter-1911/GoudyBookletter1911.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/junction/Junction-bold.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/junction/Junction-light.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/junction/Junction-regular.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/knewave/knewave-outline.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/knewave/knewave.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-gothic/LeagueGothic-CondensedItalic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-gothic/LeagueGothic-CondensedRegular.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-gothic/LeagueGothic-Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-gothic/LeagueGothic-Regular.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-script-number-one/LeagueScriptNumberOne.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/linden-hill/Linden Hill Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/linden-hill/Linden Hill.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/orbitron/Orbitron Black.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/orbitron/Orbitron Bold.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/orbitron/Orbitron Light.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/orbitron/Orbitron Medium.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSans-Black.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSans-Bold.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSans-Light.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSans-Medium.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSansDashed-Medium.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSansInline-Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSansInline-Regular.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/ostrich-sans/OstrichSansRounded-Medium.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/prociono/Prociono.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/raleway/Raleway Thin.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/sniglet/Sniglet Regular.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/sorts-mill-goudy/OFLGoudyStM-Italic.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/sorts-mill-goudy/OFLGoudyStM.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"
  install -Dm644 "$srcdir/league-spartan/LeagueSpartan-Bold.otf" "$pkgdir/usr/share/fonts/theleagueofmoveabletype"


  install -d "$pkgdir/usr/share/licenses/$pkgname"
  install -Dm644 "$srcdir/licenses/ofl.txt" "$pkgdir/usr/share/licenses/$pkgname/OFL"
}
