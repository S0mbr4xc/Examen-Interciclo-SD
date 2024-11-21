FROM debian:latest

RUN apt-get update && apt-get install -y apache2 && apt-get clean

COPY default.conf /etc/apache2/sites-available/000-default.conf

COPY dist/frontend/browser/* /var/www/html/

RUN a2enmod rewrite

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
