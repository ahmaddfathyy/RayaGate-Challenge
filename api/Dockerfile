# Dockerfile for Laravel API
# Use official PHP image with necessary extensions
FROM php:8.1-fpm

# Set working directory
WORKDIR /var/www/html

# Install system dependencies and PHP extensions
RUN apt-get update && apt-get install -y \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    zip \
    curl \
    git \
    && docker-php-ext-install pdo_mysql mbstring exif pcntl bcmath gd

# Install Composer
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# Copy the Laravel project files
COPY . .

# Install Laravel dependencies
RUN composer install --prefer-dist --no-dev --no-scripts --no-progress --no-interaction && composer fund

# Set permissions
RUN chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html/storage

# Expose port 9000 for PHP-FPM
EXPOSE 9000

CMD ["php-fpm"]
