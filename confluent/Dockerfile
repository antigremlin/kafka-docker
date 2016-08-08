FROM jdk8:latest

RUN rpm --import http://packages.confluent.io/rpm/3.0/archive.key
COPY confluent.repo /etc/yum.repos.d/
RUN yum -y install confluent-platform-2.11 && yum -y clean all