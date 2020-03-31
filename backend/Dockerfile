FROM ruby:2.7.0-slim

# "man" dirs creation prevents fail when install postgresql-client
# Try to remove them when decide to upgrade an image
RUN apt-get update -qq \
    && mkdir -p /usr/share/man/man1 \
    && mkdir -p /usr/share/man/man7 \
    && apt-get install \
    -y --no-install-recommends git build-essential libpq-dev postgresql-client \
    && rm -rf /var/lib/apt/lists/*

ENV WEB_ROOT /backend
RUN mkdir $WEB_ROOT
WORKDIR $WEB_ROOT
