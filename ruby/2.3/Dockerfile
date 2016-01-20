FROM ruby:2.3.0

RUN apt-get update \
 && apt-get install -y --no-install-recommends nodejs mysql-client sqlite3 \
 && rm -rf /var/lib/apt/lists/*

CMD [ "irb" ]
