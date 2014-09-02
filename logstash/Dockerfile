FROM ubuntu:14.04
MAINTAINER Shawn Oakley <shawnoakley@gmail.com>
ENV REFRESEHED_AT 2014-09-02

RUN apt-get -yqq update
RUN apt-get -yqq install wget
RUN wget -O - http://packages.elastcsearch.org/GPG-KEY-elasticsearch | apt-key add -
RUN echo 'deb http://packages.elasticsearch.org/logstash/1.4/debian stable main' > /etc/apt/sources.list.d/logstash.list
RUN apt-get -yqq update
RUN apt-get -yqq install logstash

ADD logstash.conf /etc/

WORKDIR /opt/logstash

ENTRYPOINT [ "bin/logstash" ]
CMD [ "--config=/etc/logstash.conf" ]