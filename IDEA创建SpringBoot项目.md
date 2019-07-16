

# IDEA创建SpringBoot项目

​	![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.25.10.png?raw=true)



next

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.29.40.png?raw=true)



![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.38.03.png?raw=true)



![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.42.59.png?raw=true)



![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.43.54.png?raw=true)

选择Enable Auto-Import 自动导入依赖



项目工程目录如下：

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%886.47.53.png?raw=true)

 ![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.06.17.png?raw=true)



在`com/example/springbootpro`目录下创建文件`helloController.java`

```java
package com.example.springbootpro;

import org.springframework.web.bind.annotation.RequestMapping;

@RestController
public class helloController {

    @RequestMapping("/hello")
    public void hello(){
        System.out.println("hello!");
    }
}
```



运行文件

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.15.53.png?raw=true)



如果出现报错`Caused by: java.net.BindException: Address already in use`

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.22.17.png?raw=true)



解决办法：

在`application.properties`文件下添加`server.port=8899`

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.25.23.png?raw=true)

再次运行：

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.28.33.png?raw=true)

浏览器地址栏中输入`localhost:8899/hello`

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.33.54.png?raw=true)

控制台输出：

![alt](https://github.com/coder-kk596/md_img/blob/master/Springboot_img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.34.31.png?raw=true)



项目创建成功。

