[TOC]



### 0 环境

​	JDK:8

​	Maven:3

### 1 spring boot启动模板项目

#### 1.1 在spring官网创建项目模板

- 访问网址：https://start.spring.io/，选择Spring Web dependence


![image-20200402181150189](./SpringBoot启动.assets/image-20200402181150189.png) 

- 点击generate后自动下载项目zip

 ![image-20200402181826158](SpringBoot启动.assets/image-20200402181826158.png)

- 在IDEA导入

![image-20200402202057855](SpringBoot启动.assets/image-20200402202057855.png)

![image-20200402202210019](SpringBoot启动.assets/image-20200402202210019.png)

#### 1.2 验证项目

- 添加/hello映射，注意一定要加@RestController，要不然mapping不起作用

```java
@SpringBootApplication
@RestController
public class SpringbootStartDemoApplication {

	public static void main(String[] args) {
		SpringApplication.run(SpringbootStartDemoApplication.class, args);
	}
	//hello world :)
	@GetMapping("/hello")
	public String hello(@RequestParam(value = "name", defaultValue = "World") String name) {
		return String.format("Hello %s!", name);
	}
}
```

- 启动服务

![image-20200402194750391](SpringBoot启动.assets/image-20200402194750391.png)  

- 测试，访问http://localhost:8080/hello

![image-20200402195415450](SpringBoot启动.assets/image-20200402195415450.png) 

### 2 将新建项目上传到github

- 添加github账号到idea

![image-20200402215311093](SpringBoot启动.assets/image-20200402215311093.png)

- 创建本地repository

![image-20200402203640008](SpringBoot启动.assets/image-20200402203640008.png)

- 选中要提交的项目目录，点击"OK"

![image-20200402203844403](SpringBoot启动.assets/image-20200402203844403.png) 

- 目录中文件变为红色

![image-20200402204035869](SpringBoot启动.assets/image-20200402204035869.png) 

- 文件目录下多了.git隐藏文件夹

![image-20200402204158546](SpringBoot启动.assets/image-20200402204158546.png) 

- 添加到git，相当于svn的add

![image-20200402204344600](SpringBoot启动.assets/image-20200402204344600.png) 

- commit文件，相当于svn的commit，只是commit到本地仓库

![image-20200402204620138](SpringBoot启动.assets/image-20200402204620138.png)

![image-20200402205003937](SpringBoot启动.assets/image-20200402205003937.png)

- push到github，执行完这一步之后才会发送到github

![image-20200402211459052](SpringBoot启动.assets/image-20200402211459052.png)

