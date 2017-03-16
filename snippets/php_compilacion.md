PHP - Compilacion
=================

## Dependencias en Ubuntu

```
sudo apt-get install libxml2-dev libssl-dev libcurl4-openssl-dev libcurl4-gnutls-dev libjpeg-turbo8-dev libpng-dev libfreetype6-dev libmcrypt-dev libreadline-dev libxslt1-dev
```

## Compilación

```
tar xzvf php-xxx
cd php-xxx
./configure \
--prefix=/usr/local/php/php_7_1_2 \
--disable-all \
--enable-phar \
--enable-session \
--enable-filter \
--enable-soap \
--enable-sockets \
--enable-bcmath \
--enable-ftp \
--enable-tokenizer \
--with-readline \
--with-zlib \
--with-curl \
--with-pear \
--enable-static \
--enable-cli \
--enable-json \
--with-iconv \
--enable-ctype \
--enable-posix \
--enable-ipv6 \
--enable-calendar \
--enable-mbstring \
--with-mcrypt \
--with-mhash \
--enable-dom \
--enable-xml \
--enable-libxml \
--enable-simplexml \
--with-libxml-dir=/usr/bin \
--enable-xmlwriter \
--enable-xmlreader \
--with-xsl \
--with-gettext \
--enable-intl \
--enable-mysqlnd \
--with-mysqli=mysqlnd \
--with-sqlite3 \
--enable-pdo \
--with-pdo-sqlite \
--enable-mysqlnd-compression-support \
--with-openssl \
--with-openssl-dir=/usr/bin \
--with-openssl-dir \
--with-gd \
--with-freetype-dir \
--with-jpeg-dir \
--with-png-dir \
--enable-fileinfo \
--enable-opcache \
--enable-zip \
--enable-inline-optimization \
--with-pdo-mysql

make
sudo make install

sudo cp php.ini-development /usr/local/php/php_7_1_2/lib/php.ini

# crear links simbolicos

cd /usr/local/php
sudo ln -s php_7_1_2 php

cd /usr/bin
sudo ln -s /usr/local/php/php/bin/*
```
