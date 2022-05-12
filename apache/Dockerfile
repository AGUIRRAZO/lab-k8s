FROM httpd:2.4.53-alpine

LABEL MAINTAINER=aguirre.asier@opendeusto.es
ADD Dockerfile /tmp/Dockerfile

WORKDIR /usr/local/apache2/conf/
COPY ./my-httpd.conf httpd.conf