FROM elasticsearch2-rhel7

USER root

RUN /usr/share/elasticsearch/bin/plugin install -b license;/usr/share/elasticsearch/bin/plugin install -b marvel-agent;/usr/share/elasticsearch/bin/plugin install -b shield;/usr/share/elasticsearch/bin/plugin install -b graph;/usr/share/elasticsearch/bin/plugin install -b watcher

USER elasticsearch
