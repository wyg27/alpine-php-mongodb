FROM php:8.0.10-cli-alpine3.13 
RUN apk --update add --no-cache \
    alpine-sdk \
    autoconf \
    zlib-dev \
    libpng-dev \
    oniguruma-dev
RUN pecl install mongodb && pecl clear-cache
RUN docker-php-ext-enable mongodb
RUN docker-php-ext-install gd
RUN docker-php-ext-install mbstring
#RUN docker-php-ext-install zip

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /app

ENTRYPOINT ["composer"]
