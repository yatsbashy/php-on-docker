FROM php:7.3.3-fpm
LABEL maintainer="yatsubashi"

# Linux
RUN apt-get update && apt-get install -y \
    curl \
    git \
    libicu-dev \
    libzip-dev \
    unzip \
    wget \
    zip \
    zlib1g-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
RUN docker-php-ext-install \
    bcmath \
    mbstring \
    mysqli \
    intl \
    pdo_mysql \
    zip

# composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
ENV COMPOSER_ALLOW_SUPERUSER 1

WORKDIR /var/www/html