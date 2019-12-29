#simple base image using apt-cacher-ng, requires an 
FROM cached-base:buster
#FROM debian:stretch
RUN apt-get update && apt-get -y dist-upgrade
RUN echo 'deb http://deb.debian.org/debian experimental main contrib non-free' > /etc/apt/sources.list.d/experimental.list
RUN apt-get update
RUN apt-get -y install -t experimental freeipa-server freeipa-client freeipa-common python-ipaserver

CMD /bin/bash
