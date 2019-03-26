FROM ruby:2.3.0

RUN echo 127.0.0.1 local.host | tee -a /etc/hosts && \
    echo 127.0.0.1 www.local.host | tee -a /etc/hosts && \
    echo 127.0.0.1 forum.local.host | tee -a /etc/hosts && \
    echo 127.0.0.1 guide.local.host | tee -a /etc/hosts && \
    echo 127.0.0.1 api.local.host | tee -a /etc/hosts && \
    echo 127.0.0.1 m.local.host | tee -a /etc/hosts

RUN sed -i 's/^.*jessie-updates/#&/' /etc/apt/sources.list && \
    apt-get update && \
    apt-get install -y --force-yes libsasl2-dev nodejs netcat mysql-client

RUN gem install bundler -v 1.14.6 && \
    gem install rainbow -v 2.2.1
