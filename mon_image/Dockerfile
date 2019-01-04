FROM php:7.2-apache
 
RUN apt-get update \
	&& docker-php-ext-install pdo mysqli \
	&& useradd -g root utilisateur \
	&& find . -name "httpd.conf" | cat | grep "DocumentRoot" -sl | sed 's/DocumentRoot/DocumentUser/g' | cat