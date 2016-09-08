FROM openjdk7-rhel7

COPY elasticsearch.repo /etc/yum.repos.d/
COPY elasticsearch.yml /etc/elasticsearch/
COPY logging.yml /etc/elasticsearch/

RUN yum -y install elasticsearch && yum clean all

USER elasticsearch

ENV PATH=$PATH:/usr/share/elasticsearch/bin
ENV ES_HOME=/usr/share/elasticsearch CONF_DIR=/etc/elasticsearch DATA_DIR=/var/lib/elasticsearch LOG_DIR=/var/log/elasticsearch ES_HOSTS=127.0.0.1

CMD ["elasticsearch","-Des.default.path.home=${ES_HOME}","-Des.default.path.logs=${LOG_DIR}","-Des.default.path.data=${DATA_DIR}","-Des.default.path.conf=${CONF_DIR}","-Des.discovery.zen.ping.unicast.hosts=${ES_HOSTS}"]

EXPOSE 9200 9300
