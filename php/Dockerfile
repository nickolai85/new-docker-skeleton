FROM php:8.0.0rc1-fpm

RUN apt-get update
RUN apt-get -y install --no-install-recommends \
        gcc \
        make \
        build-essential \
        autoconf \
        libssl-dev \
        git \
        bash \
        nano \
        wget \
        libc-dev \
        pkg-config \
        librabbitmq-dev \
        libmcrypt-dev \
        zlib1g-dev \
        libicu-dev \
        g++ \
        libpng-dev \
        zip \
        curl \
        imagemagick \
        libfreetype6-dev \
        libcurl3-dev \
        libjpeg-dev \
        libjpeg62-turbo-dev \
        libmagickwand-dev \
        libpq-dev \
        libxml2-dev \
        libzip-dev \
        openssh-client \
        unzip && \
    rm -rf /var/lib/apt/lists/* && \
    apt-get clean

RUN docker-php-ext-install \
        zip \
        curl \
        gd \
        opcache \
        pdo_mysql \
        bz2 \
        gettext

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer