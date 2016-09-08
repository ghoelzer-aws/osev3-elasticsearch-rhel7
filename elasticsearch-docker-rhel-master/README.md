# elasticsearch-docker-rhel
dockerfiles for rhel based images

Build:

go to developers.redhat.com and get a free development subscription

install a rhel7 os

install docker

docker build -t openjdk7-rhel7 openjdk-rhel7

docker build -t elasticsearch2-rhel7 elasticsearch2

Run like:

  docker run -d -p 9202:9200 -p 9302:9300 -e "ES_HOSTS=172.17.0.4,172.17.0.3" elasticsearch2-rhel7
  
  Where the ip addresses are correct for your containers in raw docker.
  
  Use kubernetes services in openshift and kubernetes for the other hosts.
  
