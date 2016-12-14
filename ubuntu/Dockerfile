FROM ubuntu:16.04

MAINTAINER hxhgta "hxhgta@163.com"

# 安装ubuntu必备的软件
RUN \
  sed -i 's/# \(.*multiverse$\)/\1/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
#  apt-get install -y build-essential && \
#  apt-get install -y software-properties-common && \
  apt-get install -y byobu curl git htop man unzip vim wget

# 安装zsh
RUN apt-get -y install zsh && \
 git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
 cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc && \
 chsh -s $(which zsh) root

# 安装 python
RUN apt-get install -y python python-dev python-pip python-virtualenv

# 安装ruby
RUN apt-get install -y ruby ruby-dev ruby-bundler

# 删除apt的缓存
RUN rm -rf /var/lib/apt/lists/*

# 配置git
ADD root/.gitconfig /root/.gitconfig

# 配置环境
ENV HOME /root

ENTRYPOINT ["/bin/zsh"]
