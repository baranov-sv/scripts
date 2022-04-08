FROM ruby:2.7.1-alpine

RUN apk add --no-cache --virtual .build-deps bash openssh-client build-base \
      postgresql-dev postgresql-client && \
    apk add --update tzdata && \
    rm -rf /var/cache/apk/*

ENV APP_PATH /usr/src/app
RUN mkdir -p $APP_PATH
RUN mkdir -p $APP_PATH/local/bundle
WORKDIR $APP_PATH

RUN rm -rf /usr/local/bundle && ln -s $APP_PATH/local/bundle /usr/local/bundle
