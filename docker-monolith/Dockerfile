FROM ubuntu:18.04
RUN apt-get update \
    && apt-get install -y mongodb-server ruby-full ruby-dev build-essential git \
    && gem install bundler
RUN git clone -b app https://github.com/AlexViki/laba_11_docker_v2.git

COPY mongod.conf /etc/mongod.conf
COPY db_config /reddit/db_config
COPY start.sh /start.sh

RUN cd /reddit && bundle install
RUN chmod 0777 /start.sh

CMD ["/start.sh"]