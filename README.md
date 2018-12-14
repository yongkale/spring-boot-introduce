# spring-boot-introduce

kale 个人理解，如有不对。希望的指导。

对spring boot的疑问:
  1. 为什么springboot没有web.xml。
  2. @SpringBootApplication的作用。
  3. springboot 为什么不需要tomcat等容器。
  
1.springboot使用Spring MVC作为MVC框架,springmvc可以通过@EnableWebMvc启动（不需要配置web.xml）。     

2:
 spring boot 启动注解@SpringBootApplication

       
3：springboot 通过maven的继承方式内嵌了tomcat等容器。

springboot打包后的文件
  
  springboot 在打包之后生成两个jar文件：
    1.以SNAPSHOT.jar为后缀的jar文件（maven默认生成的jar）
    2.以SNAPSHOT.jar.original为后缀的jar文件(spring boot maven插件生成的jar包,包含依赖等)
 
