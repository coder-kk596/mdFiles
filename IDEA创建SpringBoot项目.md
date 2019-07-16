

# IDEA创建SpringBoot项目

​	![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午6.25.10.png)



next

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午6.29.40.png)



![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午6.38.03.png)



![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午6.42.59.png)



![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午6.43.54.png)

选择Enable Auto-Import 自动导入依赖



![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.06.17.png)

 

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

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.32.12.png)



如果出现报错`Caused by: java.net.BindException: Address already in use`

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.22.17.png)



解决办法：

在`application.properties`文件下添加`server.port=8899`

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.25.23.png)

再次运行：

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.28.33.png)

浏览器地址栏中输入`localhost:8899/hello`

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.33.54.png)

控制台输出：

![alt](/Users/coder/Desktop/Springboot_img/屏幕快照 2019-07-16 下午7.34.31.png)



项目创建成功。