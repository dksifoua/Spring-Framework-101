# Spring Framework 6

## About Spring Framework

- Spring Framework is the most popular Java framework for building enterprise grade applications
- Enterprise grade being highly scalable and reliable applications
  - Over 60% of companies using Java use Spring
- Highly popular with banks, financial institutions, and large retailers
- Can be used for traditional monolithic applications
- Well suited for modern microservice based architectures
- Commonly used as the **backend** technology

## History of Spring Framework

- Introduced by Rod Johnson in 2003
  - Started as a simple alternative to J2EE
  - Rod authored a book called **Expert One on One J2EE without EJB**
  - EJB - Enterprise Java Beans, aka **XML Hell**
  - Focus was on using POJOs to simplify development
- March 2004 - Spring Framework 1.0 released
- 2007 - Spring Framework 2.5 released with Annotation based configuration
- August - 2009 Spring Source purchased by VMWare for $420 Million
- December 2009 - Spring 3.0 released with Java based configuration
- April 2013 - VMWare form a new company, Pivotal. All Spring applications was moved to this company.
- April 2014 - Spring Boot 1.0 released
- July 2017 - Spring Framework 5 released, Introduction to Reactive Programming
- Nov 2017 - Spring Boot 2.0 released
- Fall 2022 - Spring Framework 6.0 released
  - Require Java 17+
  - Spring Framework 5.x supports Java 8 - Java 17
 - Fall 2022 - Spring Boot 3.0 released

## Spring Framework vs Spring Boot

- **Spring Framework** is a collection of Spring libraries
  - Dependency Injection, Web, Transaction management, etc.
- **Spring Boot** is a automated tool for Spring Framework applications
  - Think of it as a wrapper around Spring
  - You can use Spring Framework without Spring Boot
  - But you cannot use Spring Boot without Spring Framework
  
 ## Spring Components
  
![image](https://user-images.githubusercontent.com/26673598/227752259-684962eb-0574-4549-a92d-9261c8044e14.png)

## Spring Boot Features

- Curated **starter** dependencies for common components
- Sensible **Auto-Configuration** based on classes found on the classpath
  - For example, it will auto-configure an in-memmory database if H2 is on the classpath
- Externalized configuration via files and environment variables
- logging auto-configuration
- Performance metrics
- Healthcheck endpoints
- Enhanced failure information

## Major Spring Projects

- **Spring Data** - Collection fo projects for persisting data to SQL and NoSQL
- **Spring Cloud** - Tools for distributed systems
- **Spring Security** - Authentication & Authorization
- **Spring Session** - Distributed web application sessions
- **Spring Integration** - Enterprise Integration Patterns
- **Spring Batch** - batch processing
- **Spring State Machine** - Open Source State machine
