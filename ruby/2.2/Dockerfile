FROM ruby:2.2

RUN apt-get update \
 && apt-get install -y --no-install-recommends nodejs mysql-client sqlite3 \
 && rm -rf /var/lib/apt/lists/*

CMD [ "irb" ]
