FROM centos:7

ENV BUILD_HOME=/usr/local/build/

#Install Docker and compose
USER root

#RUN curl -sSL https://get.docker.com/ | sh \
RUN yum install -y yum-utils device-mapper-persistent-data lvm2 \
  && yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo \
  && yum-config-manager --enable docker-ce-edge \
  && yum makecache fast \
  && yum install -y docker-ce-17.05.0.ce-1.el7.centos \
  && curl -L https://github.com/docker/compose/releases/download/1.13.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose \
  && chmod +x /usr/local/bin/docker-compose

#Install git
RUN yum install -y git

RUN mkdir -p $BUILD_HOME
WORKDIR $BUILD_HOME
