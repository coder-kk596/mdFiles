# Centos利用Docker部署Nginx+uWSGI+Django环境



## 一.本地制作镜像

### 1.终端进入本地项目根目录

`cd /User/coder/PycharmProjects`



### 2.当前的环境依赖包导出到requirements.txt文件

`pip freeze > requirements.txt`



### 3.创建Dockerfile文件

`touch Dockerfile`

​	FROM python:3.7
​	RUN mkdir -p /usr/src/app
​	WORKDIR /usr/src/app
​	COPY pip.conf /root/.pip/pip.conf
​	COPY requirements.txt /usr/src/app/
​	RUN pip install -r /usr/src/app/requirements.txt
​	RUN rm -rf /usr/src/app
​	COPY . /usr/src/app
​	CMD [ "python", "./manage.py", "runserver", "0.0.0.0:8080"]



### 4.制作镜像images

`docker build -t my_django_pro .`

![alt](/Users/coder/Desktop/vultr_img/屏幕快照 2019-07-15 上午1.32.09.png)







## 一.Docker安装及测试



### 1.Centos中安装Docker

参考网址：[Centos安装Docker](https://www.runoob.com/docker/centos-docker-install.html)



### 2.启动Docker后台服务

`sudo systemctl start docker`



### 3.测试运行

`docker run hello-world`

![alt](/Users/coder/Desktop/vultr_img/屏幕快照 2019-07-14 下午11.23.21.png)



### 4.设置开机自动启动Docker

`sudo systemctl start docker`



## 二.安装docker-compose

docker-compose是一个用来把docker自动化的东西。有了docker-compose 你可以把所有繁琐的docker操作全都一条命令，自动化的完成。

`pip install docker-compose`

若出现	 `-bash: pip: command not found`

要先用yum安装pip

`yum install python-pip`







## 二.部署

### 1.创建Python镜像

可以先使用命令`docker search python`查看镜像

`docker pull python:3,7.4`

![alt](/Users/coder/Desktop/vultr_img/屏幕快照 2019-07-15 上午12.06.54.png)



### 2.创建MySQL镜像

`docker pull mysql:5.7`

![alt](/Users/coder/Desktop/vultr_img/屏幕快照 2019-07-15 上午12.09.42.png)



### 3.