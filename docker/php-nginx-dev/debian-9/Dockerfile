#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/php-nginx-dev:debian-9
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/php-dev:debian-9

MAINTAINER info@webdevops.io
LABEL vendor=WebDevOps.io
LABEL io.webdevops.layout=7
LABEL io.webdevops.version=0.50.0

ENV WEB_DOCUMENT_ROOT  /app
ENV WEB_DOCUMENT_INDEX index.php
ENV WEB_ALIAS_DOMAIN   *.vm

COPY conf/ /opt/docker/

# Install nginx
RUN /usr/local/bin/apt-install \
        nginx \
    && /opt/docker/bin/provision run --tag bootstrap --role webdevops-nginx --role webdevops-php-nginx --role webdevops-php-nginx-dev \
    && /opt/docker/bin/bootstrap.sh


EXPOSE 80 443
