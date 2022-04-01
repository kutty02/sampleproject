# sampleproject
Creating a php project 
Created a sample php file with the source code 
Created a Dockerfile: FROM php:7.3-apache

#Install git and MySQL extensions for PHP

RUN apt-get update && apt-get install -y git
RUN docker-php-ext-install pdo pdo_mysql mysqli
RUN a2enmod rewrite

COPY sample.php /var/www/html/
EXPOSE 80/tcp
EXPOSE 443/tcp

Did a docker build and docker run to create a container named myphpcontainer
Added, commited and pushed the php files to the repository 
