# IDEA创建Gradle文件

本地安装好Gradle后，创建新项目。

![alt](/Users/coder/Desktop/gradlePro_img/屏幕快照 2019-07-11 下午10.32.09.png)



添加本地jdk路径。

![alt](/Users/coder/Desktop/gradlePro_img/屏幕快照 2019-07-11 下午10.25.54.png)



选择本地Gradle路径

![alt](/Users/coder/Desktop/gradlePro_img/屏幕快照 2019-07-11 下午10.46.23.png)



![alt](/Users/coder/Desktop/gradlePro_img/屏幕快照 2019-07-11 下午10.49.22.png)



![alt](/Users/coder/Desktop/gradlePro_img/屏幕快照 2019-07-11 下午11.04.04.png)











plugins

https://plugins.gradle.org/





​	`build.gradle`

```java
buildscript {
    repositories {
        maven { url 'https://maven.aliyun.com/repository/public' }
        mavenCentral()
    }
    dependencies {
        classpath("org.springframework.boot:spring-boot-gradle-plugin:2.1.1.RELEASE")
    }
}

plugins {
    id 'java'
    id "org.springframework.boot" version "2.1.6.RELEASE"
}

apply plugin: 'idea'
apply plugin: 'java'
apply plugin: 'org.springframework.boot'
apply plugin: 'io.spring.dependency-management'

group 'com.lidig.myPro'
version '1.0-SNAPSHOT'

sourceCompatibility = 1.8

repositories {
    maven { url 'https://maven.aliyun.com/repository/public' }
    mavenCentral()
}


dependencies {
    compile 'org.springframework.boot:spring-boot-starter-web'
    testCompile 'org.springframework.boot:spring-boot-starter-test'
    testCompile group: 'junit', name: 'junit', version: '4.12'
}
```



在路径 `/src/main/java/com/lidig/first` 创建入口文件 `hello.java`

```java
package com.lidig.first;


import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class hello {

    public static void main(String[] args){

        SpringApplication.run(hello.class, args);

    }

}
```



新建项目下载慢

/用户/coder/.gradle



