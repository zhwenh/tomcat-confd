FROM tomcat

MAINTAINER derk@muenchhausen.de

ENV ETCD_NODE docker_etcdservice_1:4001

RUN wget https://github.com/kelseyhightower/confd/releases/download/v0.10.0/confd-0.10.0-linux-amd64 -O /usr/local/bin/confd && chmod +x /usr/local/bin/confd

ADD entrypoint.sh /entrypoint.sh
ADD confd /etc/confd

CMD ["/entrypoint.sh"]

EXPOSE 8080