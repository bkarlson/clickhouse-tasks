FROM amazonlinux:latest

RUN yum install aws-cli -y
RUN yum install perl-libwww-perl -y
RUN yum install wget -y
RUN yum install java-1.8.0-openjdk -y
RUN wget "http://apache-mirror.rbc.ru/pub/apache/zookeeper/zookeeper-3.4.9/zookeeper-3.4.9.tar.gz"
RUN tar -xzf "zookeeper-3.4.9.tar.gz"
RUN rm "zookeeper-3.4.9.tar.gz"
ADD ./entrypoint.sh ./entrypoint.sh
RUN chmod +x ./entrypoint.sh

ENTRYPOINT ["./entrypoint.sh"]
