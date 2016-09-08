FROM rhel7:latest
RUN yum repolist;yum-config-manager --disable rhel-7-server-rt-beta-rpms;yum clean all
RUN yum -y install java-1.7.0-openjdk-headless.x86_64 && yum clean all
