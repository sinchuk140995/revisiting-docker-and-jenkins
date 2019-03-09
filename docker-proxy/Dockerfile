FROM centos:centos7
LABEL maintainer="sinchuk140995@gmail.com"

RUN yum -y socat && \
    yum clean all

VOLUME /var/run/docker.sock

# Docker TCP port
EXPOSE 2375

ENTRYPOINT ["socat", "TCP-LISTEN:2375,reuseaddr,fork","UNIX-CLIENT:/var/run/docker.sock"]
