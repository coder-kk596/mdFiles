# Mac配置jdk环境

## 1.下载jdk1.8

[点击下载](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

下载地址：https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%887.10.59.png?raw=true)

## 2.安装

![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%887.50.32.png?raw=true)

![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%887.50.49.png?raw=true)

## 3.配置环境变量

__jdk安装成功后，获取路径__

![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%887.52.49.png?raw=true)



![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%888.04.44.png?raw=true)

`/Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/Contents/Home`

__将路径添加到PATH环境变量中__

终端输入`vi ./.bash_profile`

![alt 下载发布包](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%888.32.40.png?raw=true)

键盘输入e，并进入`insert`模式

添加环境变量

`export PATH=PATH:/Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/`

`Contents/Home`



![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%888.29.57.png?raw=true)



保存并退出

命令行输入`source ./.bash_profile`使环境变量生效。

`java -version`检验jdk1.8是否安装成功。输出以下内容说明安装成功。

![alt](https://github.com/coder-kk596/md_img/blob/master/jdk_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-11%20%E4%B8%8B%E5%8D%888.50.10.png?raw=true)

