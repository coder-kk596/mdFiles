# Mac配置jdk环境

## 1.下载jdk1.8

[点击下载](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

下载地址：https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

## 2.安装

![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午7.50.32.png)

![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午7.50.49.png)

## 3.配置环境变量

__jdk安装成功后，获取路径__

![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午7.52.49.png)



![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午8.04.44.png)

`/Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/Contents/Home`

__将路径添加到PATH环境变量中__

终端输入`vi ./.bash_profile`

![alt 下载发布包](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午8.32.40.png)

键盘输入e，并进入`insert`模式

添加环境变量

`export PATH=PATH:/Library/Java/JavaVirtualMachines/jdk1.8.0_211.jdk/`

`Contents/Home`

![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午8.29.57.png)

保存并退出

命令行输入`source ./.bash_profile`使环境变量生效。

`java -version`检验jdk1.8是否安装成功。输出以下内容说明安装成功。

![alt](/Users/coder/Desktop/jdk_img/屏幕快照 2019-07-11 下午8.50.10.png)