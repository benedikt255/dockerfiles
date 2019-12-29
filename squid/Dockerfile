#simple image for apt-cacher
FROM cached-base:stable
#get package list
RUN apt-get update && apt-get upgrade -y

#get apt-cacher
RUN apt-get -y install squid

COPY entrypoint.sh /sbin/entrypoint.sh
RUN chmod 755 /sbin/entrypoint.sh

EXPOSE 3128/tcp
ENTRYPOINT ["/sbin/entrypoint.sh"]
