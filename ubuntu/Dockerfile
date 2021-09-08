FROM php:latest
RUN pecl install mongodb \
    && apt-get update -y \
    && apt-get install -y \
    zlib1g-dev \
    libpng-dev \
    libonig-dev \
    libzip-dev \
    && docker-php-ext-enable mongodb \
    && docker-php-ext-install gd
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install zip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /app

ENTRYPOINT ["composer"]
