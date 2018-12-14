# spring-boot-introduce

kale

first:
 spring boot 启动注解@SpringBootApplication
 
    @SpringBootApplication = @Configuration + @EnableAutoConfiguration + @ComponentScan。
         @Configuration: 标识这个类可以使用Spring IoC容器作为bean定义的来源。
         @EnableAutoConfiguration: 能够自动配置spring的上下文，试图猜测和配置你想要的bean类，通常会自动根据你的类路径和你的bean定义自动配置。
         @ComponentScan:对包的扫描。
