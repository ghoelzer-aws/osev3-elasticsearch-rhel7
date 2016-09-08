FROM rhel7

RUN yum repolist;yum-config-manager --disable rhel-7-server-rt-beta-rpms;yum clean all
COPY beats.repo /etc/yum.repos.d/
RUN yum -y install filebeat && yum clean all
COPY filebeat.yml /etc/filebeat/
CMD /usr/bin/filebeat -c /etc/filebeat/filebeat.yml
