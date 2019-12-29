#simple image for apt-cacher
#FROM debian:stretch
FROM cached-base:latest
#get package list
RUN apt-get update && apt-get upgrade -y

#get apt-cacher
RUN apt-get -y install task-web-server
VOLUME ["/var/www/html"]
EXPOSE 80

#setup avahi, makes more sense on host
#RUN apt-get -y install squid-deb-proxy-client
#EXPOSE 53

CMD     /bin/bash
