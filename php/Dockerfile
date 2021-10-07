#Dokerfile
#Sarting from a php apache image
FROM php:7.4-apache

#Composer instalation in this image
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Need zip extention to intall symfony with composer
# Install unzip utility and libs needed by zip PHP extension 
RUN apt update && apt install -y \
    zlib1g-dev \
    libzip-dev \
    unzip
RUN docker-php-ext-install zip


#Specificating the working directory
WORKDIR /var/www/