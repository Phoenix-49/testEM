# Use the official PHP image
FROM php:8.1-fpm

# Install necessary extensions
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg-dev \
    libfreetype6-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install pdo pdo_mysql mysqli gd

# Set the working directory
WORKDIR /var/www/html

# Copy the PHP source code
COPY src/ /var/www/html
