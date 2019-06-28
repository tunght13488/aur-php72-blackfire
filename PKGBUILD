# Maintainer: Jérôme Deuchnord <jerome@deuchnord.fr>
# Contributor: Morris Jobke <hey AT morrisjobke DOT de>
pkgname=php72-blackfire
pkgver=1.26.1
pkgrel=1
pkgdesc='Blackfire Profiler - PHP extension'
arch=('i686' 'x86_64')
url='https://blackfire.io'
license=('custom')
backup=('etc/php72/conf.d/blackfire.ini')
depends=('glibc' 'php>=7.2.0' 'php<7.3')

# Change this if you need to support an older version of PHP (think to update the SHA256 sums too)
PHP_VERSION=72

source=('blackfire.ini')
source_i686=("blackfire.so-${pkgver}_${PHP_VERSION}_i686::http://packages.blackfire.io/binaries/blackfire-php/$pkgver/blackfire-php-linux_i386-php-${PHP_VERSION}.so")
source_x86_64=("blackfire.so-${pkgver}_${PHP_VERSION}_x86_64::http://packages.blackfire.io/binaries/blackfire-php/$pkgver/blackfire-php-linux_amd64-php-${PHP_VERSION}.so")

sha256sums=('90f4f316c817bd3fd37be794df645b3bc3480c167c92191e51c2decba7b4d352')
sha256sums_i686=('792a426ec29f88522c13e6c3acaa64fe7e9c65269cc64b7c7713b92b85c45c64')
sha256sums_x86_64=('3b552bf1975af4cab24ef6964eb2e9ace7ef2626cae56c7133d284a2d802431f')

package(){
  install -Dm 644 blackfire.ini "$pkgdir"/etc/php72/conf.d/blackfire.ini
  install -Dm 755 blackfire.so-${pkgver}_${PHP_VERSION}_$CARCH "$pkgdir"/usr/lib/php72/modules/blackfire.so
}
