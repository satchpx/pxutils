FROM ubuntu:14.10
MAINTAINER satchpx@gmail.com

RUN sed -i -e 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get -y update && apt-get -y install fio wget sysstat iperf

VOLUME /tmp/fio-data
RUN mkdir -p /opt/pwx/bin
COPY bin/* /opt/pwx/bin/.
RUN chmod +x /opt/pwx/bin/*

WORKDIR /tmp/fio-data
CMD ["/opt/pwx/bin/run-fio"] 
