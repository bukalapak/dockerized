FROM ubuntu:16.04
MAINTAINER Alif Rachmawadi <subosito@bukalapak.com>

RUN apt-get update \
 && DEBIAN_FRONTEND=noninteractive apt-get install -y curl apt-transport-https

RUN curl -L https://facebook.github.io/mcrouter/debrepo/xenial/PUBLIC.KEY | apt-key add \
 && echo "deb https://facebook.github.io/mcrouter/debrepo/xenial xenial contrib" >> /etc/apt/sources.list \
 && apt-get update \
 && DEBIAN_FRONTEND=noninteractive apt-get install -y mcrouter

VOLUME /var/mcrouter/fifos
VOLUME /var/spool/mcrouter

ENTRYPOINT ["mcrouter"]
