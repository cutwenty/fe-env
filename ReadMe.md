# fe-env

## ubuntu

基本的 ubuntu 系统，安装了 git、vim、zsh、python、ruby。

git 的配置在 ./ubuntu/root/.gitconfig 中，自己修改，也许可以把 .zshrc 也放到 root 文件夹中自己配置。

## nodejs

安装了 nodejs、yarn。

## gulp-webpack-runtime

全局安装了 gulp。

在 fe-env 主文件夹下

	docker build -t hxhgta/gulp-webpack-runtime -f ./gulp-webpack-runtime/Dockerfile ./gulp-webpack-runtime

创建 image 后，在项目主目录执行

	docker run -it --rm -p 80 -v 项目目录:/app hxhgta/gulp-webpack-runtime
	
之后，在 shell 里执行 gulp，打开 gulp，在本机中就写代码吧。