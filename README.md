# springmvc-helloword
springmvc框架写的简单helloword

  Spring Web MVC是一种基于Java的实现了Web MVC设计模式的请求驱动类型的轻量级Web框架，即使用了MVC架构模式的思想，将web层进行职责解耦，基于请求驱动指的就是使用请求-响应模型，框架的目的就是帮助我们简化开发，Spring Web MVC也是要简化我们日常Web开发的。
  
  主要配置好web.xml及web.xml里写的拦截设置，如在web.xml下有：
  <servlet-mapping>  
        <servlet-name>dispatcher</servlet-name>  
        <!-- 由SpringMVC拦截所有请求 -->  
        <url-pattern>/</url-pattern>  
    </servlet-mapping>  
那么就要创建一个dispatcher-servlet.xml的文件，配置完dispatcher-servlet.xml之后就控制器了，也就是java代码。
最后创建视图就完成啦。

我参考的详细的页面：

https://my.oschina.net/gaussik/blog/513353

