FROM hxhgta/nodejs

MAINTAINER hxhgta "hxhgta@163.com"

# 安装gulp
RUN npm install -g gulp

# 运行docker run -d -p 80 -v ./:/app hxhgta/gulp-webpack-runtime
# -d后台运行
# -p 打开端口，这两个可以看着办

# 配置项目根目录
WORKDIR /app

# 配置环境
# RUN yarn install
# RUN gulp

# 配置输出端口
EXPOSE 80

ENTRYPOINT yarn install && /bin/zsh
