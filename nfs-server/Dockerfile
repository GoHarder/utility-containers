FROM debian:stable-slim

RUN apt-get update
RUN apt-get install -y nfs-kernel-server portmap

COPY exports /etc/exports

EXPOSE 2049
EXPOSE 111

ADD run /usr/local/bin/run
RUN chmod u+x /usr/local/bin/run
ENTRYPOINT [ "run" ]