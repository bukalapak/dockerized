FROM ruby:2.2

RUN apt-get update && apt-get install -y nodejs mysql-client sqlite3 --no-install-recommends && rm -rf /var/lib/apt/lists/*

ENV RAILS_VERSION 4.1.14

RUN gem install rails --version "$RAILS_VERSION"