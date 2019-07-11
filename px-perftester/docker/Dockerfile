FROM ubuntu:14.10
MAINTAINER satchpx@gmail.com

RUN sed -i -e 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get -y update && apt-get -y install fio wget sysstat iperf

VOLUME /tmp/fio-data
RUN mkdir -p /opt/msi/bin
COPY ../bin/* /opt/msi/bin/.
RUN chmod +x /opt/msi/bin/*

WORKDIR /tmp/fio-data
CMD ["/opt/msi/bin/run-fio"] 
