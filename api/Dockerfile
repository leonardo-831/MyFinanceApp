FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    libpng-dev \
    zip \
    unzip \
    curl \
    git \
    libpq-dev \
    && docker-php-ext-install pdo pdo_pgsql gd

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www

COPY . .

EXPOSE 9000

CMD ["php-fpm"]
