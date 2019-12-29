#simple image for apt-cacher
FROM debian:stable
#get package list
RUN apt-get update && apt-get upgrade -y

#get apt-cacher
RUN apt-get -y install apt-cacher-ng
VOLUME ["/var/cache/apt-cacher-ng"]
EXPOSE 3142

#setup avahi, makes more sense on host
#RUN apt-get -y install squid-deb-proxy-client
#EXPOSE 53

CMD     chmod 777 /var/cache/apt-cacher-ng && /etc/init.d/apt-cacher-ng start && tail -f /var/log/apt-cacher-ng/*
