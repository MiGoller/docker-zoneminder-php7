# Docker image of zoneminder with API-support
This images stays up to date with the original one but enables API-support on PHP7.x. Enjoy.

Starting with PHP 7.0, APCu removed the option for full backwards compatibility with APC that existed with APCu in PHP 5.5 and 5.6.
You will need to add the APCu Backwards Compatiblity Module on top of apcu to make it work. (https://pecl.php.net/package/apcu_bc)

kylejohnson's docker image is based on Ubuntu 16.04, so we will have to run the following commands.
```sh
apt-get install php7.0-opcache php-apcu software-properties-common

add-apt-repository "deb http://ftp.de.debian.org/debian sid main"
apt-get update
apt-get install php-apcu-bc
```
  
To build the image just run:
```sh
docker build -t [username]/[imagename] .
```

## Thanx to kylejohnson for his basic docker image.
