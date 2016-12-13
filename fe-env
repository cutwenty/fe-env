FROM ubuntu:16.04

MAINTAINER hxhgta "hxhgta@163.com"

# 安装ubuntu必备的软件
RUN \
  sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y build-essential && \
  apt-get install -y software-properties-common && \
  apt-get install -y byobu curl git htop man unzip vim wget && \
  rm -rf /var/lib/apt/lists/*

# 创建项目根目录
RUN mkdir /app
ENV HOME /app
WORKDIR /app

CMD ["bash"]
