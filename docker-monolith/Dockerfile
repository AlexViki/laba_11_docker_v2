FROM ubuntu:18.04
RUN apt-get update \
    && apt-get install -y mongodb-server ruby-full ruby-dev build-essential git \
    && gem install bundler
RUN git clone https://github.com/express42/reddit.git 