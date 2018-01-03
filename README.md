# springmvc-helloword
springmvc框架写的简单helloword

  Spring Web MVC是一种基于Java的实现了Web MVC设计模式的请求驱动类型的轻量级Web框架，即使用了MVC架构模式的思想，将web层进行职责解耦，基于请求驱动指的就是使用请求-响应模型，框架的目的就是帮助我们简化开发，Spring Web MVC也是要简化我们日常Web开发的。
  
  主要配置好web.xml及web.xml里写的servlet级的拦截设置，如在web.xml下有：
``` java
  ...
  <servlet>
        <servlet-name>dispatcher</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
        <init-param>
            <param-name>contextConfigLocation</param-name>
            <param-value>WEB-INF/applicationContext.xml</param-value>
        </init-param>
        <load-on-startup>1</load-on-startup>
    </servlet>
    <servlet-mapping>
        <servlet-name>dispatcher</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
    ...
```
创建一个applicationContext.xml的配置文件
```java
    ...
    <context:component-scan base-package="com.controller"/>
    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
        <property name="prefix" value="/WEB-INF/pages/"/>
        <property name="suffix" value=".jsp"/>
    </bean>
    ...
```
applicationContext.xml的内容有一个扫描com.controller包下的bean的component-scan标签，若包内有带有自动装配注解（如：@Controller）的类，spring会自动装配该类。<br>
applicationContext.xml还配置了一个InternalResourceViewResolver的bean，功能是给controller返回的值添加前缀和后缀，使spring能确定视图资源的具体位置。
<br>


