#一、Gradle 简介
是一个基于 JVM 附有突破性构建工具。
#二、Gradle 概述

#三、配置Gradle环境
###1、官网上下载 Gradle 最新发布包
[http://services.gradle.org/distributions/](http://services.gradle.org/distributions/)

![alt 下载发布包](./Gradle_img/gra1.png)

###2、解压 ZIP 文件
将解压后的文件放到`/usr/local` 下 

###3、配置环境变量
#### 将 gradle/bin 添加到 PATH 环境变量中 
`vi ./.bash_profile`

![alt 下载发布包](./Gradle_img/gra2.png)

#### 输入 E，并进入 `insert` 模式

![alt 下载发布包](./Gradle_img/gra3.png)

#### 添加环境变量

`export PATH=$PATH:/usr/local/gradle/bin`

`source ./.bash_profile`

使环境变量生效

#### 测试安装  
`gradle -v`

![alt 下载发布包](./Gradle_img/gra4.png)

#### JVM 参数配置







# IDEA创建Gradle项目





# 四、Gradle 构建基础
### 1、构建基础
#### Project 和 tasks
Project 和 tasks 是 Gradle 中最重要的两个概念。任何一个 Gradle 构建都是由一个或多个 projects 组成。每个 project 包括许多可构建组成部分。这完全取决于你要构建些什么。举个例子，每个 project 或许是一个 jar 包或者一个 web 应用，它也可以是一个由许多其他项目中产生的 jar 构成的 zip 压缩包。一个 project 不必描述它只能进行构建操作。它也可以部署你的应用或搭建你的环境。不要担心它像听上去的那样庞大。Gradle 的 build-by-convention 可以让您来具体定义一个 project 到底该做什么。
每个 project 都由多个 tasks 组成。每个 task 都代表了构建执行过程中的一个原子性操作。如编译，打包，生成 javadoc，发布到某个仓库等操作。

#### 第一个构建脚本
新建 Gradle 项目文件夹，编写第一个脚本。
目录`/gradlePro/pro_0710` 下创建 `build.gradle`

	task hello{
		doLast{
			println 'Hello world!'
		}
	}

在该文件下执行命令 `gradle -q hello`

命令行显示 `Hello world!`

-q 参数用来控制 gradle 的日志级别，可以保证只输出我们需要的内容。---
### 2、快速定义任务
一种更为简洁的方式定义 hello 任务
#### 快速定义任务
	task hello{ 
		println 'Hello world!'
	}
__tips__:（快捷键（<<符号表示）在 Gradle5.0 已被移除）  
采用闭包的方式定义 `hello` 任务	

Gradle 脚本采用 Groovy 书写
---
### 3、在 gradle 任务中采用 groovy
例子 1:

	task hello{ 
		String x = "hello world"
		println "Original:" + x
		println "Upper case:" + x.toUpperCase()
	} 

运行结果：

![alt 运行结果](/Users/coder/desktop/Gradle_img/gra5.png)

例子 2:

	task hello{ 
		4.times {
			print "$it "
		}
	} 

运行结果：

![alt 运行结果](/Users/coder/desktop/Gradle_img/gra6.png)
---
### 4、任务依赖
#### 在两个任务之间指明依赖关系

	task hello{ 
		println "hello world"
	} 
	
	task lkk(dependsOn: hello){
		println "I'm lkk"
	}
输入命令：`gradle -q hello`

运行结果：

![alt 运行结果](/Users/coder/desktop/Gradle_img/gra7.png)
---
### 5、延迟依赖
	task first(dependsOn: 'second'){ 
		println "first"
	} 
	task second{
		println "second"
	}
输入命令：`gradle -q first`

运行结果：

![alt 运行结果](./Gradle_img/gra8.png)

### 6、动态任务
#### 创建动态任务
	4.times { counter ->
		task "task$counter" {
			println "I'm task number $counter"
		}
	}
命令：`gradle -q task0|task1|task2|task3`
运行结果：

![alt 运行结果](./Gradle_img/gra9.png)

### 7、任务操纵

