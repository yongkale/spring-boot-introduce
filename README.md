# spring-boot-introduce

kale 个人理解，如有不对。希望的指导。

对spring boot的疑问:
  1. 为什么springboot没有web.xml。
  2. @SpringBootApplication的作用。
  3. springboot 为什么不需要tomcat等容器。
  
1.springboot使用Spring MVC作为MVC框架,springmvc可以通过@EnableWebMvc启动（不需要配置web.xml）。     

2:
 spring boot 启动注解@SpringBootApplication
 
    ```@SpringBootApplication = @Configuration + @EnableAutoConfiguration + @ComponentScan。
         I. @SpringBootConfiguration: 代表了SpringBoot的配置类，其本质上就是一个@Configuration。
                @SpringBootConfiguration与@Configuration
                    唯一不同的地方是在测试时，如果打上了@SpringBootConfiguration注释，那么SpringBootTest中并不需要指定就可以自动加载该配置类；而当                     打上@Configuration时，需要通过@SpringBootTest(classes = SBConfiguration.class)来指定加载的SpringBoot配置类。
         II. @EnableAutoConfiguration: 能够自动配置spring的上下文，试图猜测和配置你想要的bean类，通常会自动根据你的类路径和你的bean定义自动配置。
         III. @ComponentScan:对包的扫描。
         
      注：如果对注解不熟悉的小伙伴可以参考（http://www.cnblogs.com/huajiezh/p/5263849.html）```
       
3：springboot 通过maven的继承方式内嵌了tomcat等容器。

springboot打包后的文件
  
  springboot 在打包之后生成两个jar文件：
    1.以SNAPSHOT.jar为后缀的jar文件（maven默认生成的jar）
    2.以SNAPSHOT.jar.original为后缀的jar文件(spring boot maven插件生成的jar包,包含依赖等)
 
