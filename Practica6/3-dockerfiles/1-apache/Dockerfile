FROM centos:7

RUN yum update -y && yum install httpd -y

COPY ./web /var/www/html

CMD [ "apachectl", "-D", "FOREGROUND" ]