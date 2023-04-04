# Spring IOC Container

## What is the Spring IOC Container?

The Spring container is responsible for instantiating, configuring, and assembling the Spring beans. The container gets its instructions on what objects to instantiate, configure, and assemble by reading configuration metadata. The configuration metadata is represented in XML, Java annotations, or Java code. It lets us express the objects that compose our application and the rich inter-dependencies between those objects.

The responsibilities of IOC container are:
- Instantiating the beans
- Wiring the beans together
- Configuring the beans
- Managing the bean’s entire life-cycle

The `org.springframework.beans` and `org.springframework.context` packages are the basis for Spring Framework’s IoC container. Spring framework provides two distinct types of containers.
- `BeanFactory` container: it is the root interface of Spring IOC container
- `ApplicationContext` container: it is the child interface of `BeanFactory` interface that provides Spring AOP features, i18n etc.

The Spring IoC container consumes a form of configuration metadata. This configuration metadata represents how we, as an application developer, tell the Spring container to instantiate, configure, and assemble the objects in our application. There are three ways we can supply Configuration Metadata to Spring IoC container:
- XML-based configuration
- Annotation-based configuration
- Java-based configuration

## Spring IOC Container with Java-based configuration

Lets create a bean class called `MyBean`.

```java
package io.dksifoua.spring.ioc;


public class MyBean {
  private String message;

  public void setMessage(String message) {
    this.message = message;
  }

  public void getMessage() {
    System.out.println("My Bean Message : " + message);
  }
}
```

Next, let's configure the `MyBean` class as Spring bean using Java-based configuration:

```java
package io.dksifoua.spring.ioc;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import io.dksifoua.spring.ioc.MyBean;


@Configuration
public class ApplicationConfiguration {

  @Bean
  public MyBean getMyBean() {
    MyBean myBean = new MyBean();
    myBean.setMessage("Hello World Bean!");
    return myBean;
  }
}
```

Spring `@Configuration` annotation is part of the spring core framework. Spring Configuration annotation indicates that the class has `@Bean` definition methods. So Spring container can process the class and generate Spring Beans to be used in the application.

Finally, we create a Spring container and retrieve the bean from it.

```java
package io.dksifoua.spring.ioc;

import org.springframework.context.annotation.AnnotationConfigApplicationContext;

import io.dksifoua.spring.ioc.ApplicationConfiguration;
import io.dksifoua.spring.ioc.MyBean;


public class SpringApplication {
  
  public static void main(String... args) {
    AnnotationConfigApplicationContext context = new AnnotationConfigApplicationContext(ApplicationConfiguration.class);
    MyBean myBean = (MyBean) context.getBean(MyBean.class);
    myBean.getMessage();
    context.close();
  }
}
```

