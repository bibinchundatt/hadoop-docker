# ubuntu 16.04

FROM ubuntu:xenial

# udpate ubuntu image
RUN apt-get update

RUN apt-get install -y curl tar sudo openssh-server openssh-client rsync

RUN mkdir -p /usr/java/default

RUN mkdir -p /usr/local/download
RUN curl --url 'http://www-eu.apache.org/dist/hadoop/common/hadoop-3.1.1/hadoop-3.1.1.tar.gz' --output /usr/local/download/hadoop.tar.gz

RUN tar -xzvf /usr/local/download/hadoop.tar.gz -C /usr/local/.

RUN mv /usr/local/hadoop* /usr/local/hadoop


# Defining env

ENV HADOOP_PREFIX /usr/local/hadoop
ENV HADOOP_COMMON_HOME /usr/local/hadoop
ENV HADOOP_HDFS_HOME /usr/local/hadoop
ENV HADOOP_MAPRED_HOME /usr/local/hadoop
ENV HADOOP_YARN_HOME /usr/local/hadoop
ENV HADOOP_CONF_DIR /usr/local/hadoop/etc/hadoop
ENV YARN_CONF_DIR $HADOOP_PREFIX/etc/hadoop





