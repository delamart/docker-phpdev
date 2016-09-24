FROM php:5.6

MAINTAINER Erik DeLamarter <erik@delamarter.ch>

RUN	apt-get update && apt-get install -y \
	git \
	libsqlite3-dev \
	libzip-dev \
	unzip \
	&& pecl install xdebug \
	&& docker-php-ext-install pdo pdo_sqlite zip \
    && docker-php-ext-enable xdebug

ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_DISABLE_XDEBUG_WARN 1	
	
RUN	curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
