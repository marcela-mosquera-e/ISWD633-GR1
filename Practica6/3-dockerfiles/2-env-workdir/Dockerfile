FROM httpd:2.4

ENV VERSION=1.0.0
ENV AUTHOR=
ENV USERNAME=

COPY ./web /var/www/html

CMD [ "apachectl", "-D", "FOREGROUND" ]