# Docker Image Builder v2
# These images are built using Dockerfile inheritance to build the images used for Probo.CI.
# Image: proboci/php
# Tag: 5.6
# Build the proboci/ubuntu:5.6 image:tag with the following command from inside the 5.6 directory where the Dockerfile lives:
# `docker build -t proboci/ubuntu:5.6 .`

FROM proboci/ubuntu:14.04

ENV PHP_VERSION 5.6
ENV WORKDIR /root

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
	language-pack-en-base \
  && LC_ALL=en_US.UTF-8 add-apt-repository ppa:ondrej/php \
  && apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
  	php$PHP_VERSION \
  	php$PHP_VERSION-cli \
  	php$PHP_VERSION-common \
  	php$PHP_VERSION-curl \
  	php$PHP_VERSION-dev \
  	php$PHP_VERSION-gd \
  	php$PHP_VERSION-json \
  	php$PHP_VERSION-ldap \
  	php$PHP_VERSION-mbstring \
  	php$PHP_VERSION-mcrypt \
  	php$PHP_VERSION-mysql \
  	php$PHP_VERSION-readline \
  	php$PHP_VERSION-xml \
  	php$PHP_VERSION-zip \
  	libapache2-mod-php$PHP_VERSION \
  	php5-imagick \
  	php-pear \
  	php-redis \
  	php-uploadprogress \
  	imagemagick \
  	libzip-dev \
  	memcached \
  	redis-server \
  && apt-get --purge autoremove language-pack-en-base -y \
  && rm -rf /var/lib/apt/lists/* /tmp/*
