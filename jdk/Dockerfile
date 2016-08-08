FROM rhel7/rhel

RUN yum install -y tar && yum -y clean all
RUN curl -s -L --header "Cookie: oraclelicense=accept-securebackup-cookie;" \
http://download.oracle.com/otn-pub/java/jdk/8u101-b13/server-jre-8u101-linux-x64.tar.gz \
| tar xz -C /opt --no-same-owner

ENV JAVA_HOME=/opt/jdk1.8.0_101
ENV PATH=$PATH:$JAVA_HOME/bin