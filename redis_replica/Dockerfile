FROM jamtur01/redis
MAINTAINER Shawn Oakley <shawnoakley@gmail.com>
ENV REFRESHED_AT 2014-09-02

ENTRYPOINT [ "redis-server", "--logfile /var/log/redis/redis-replica.log", "--slaveof redis_primary 6379"]