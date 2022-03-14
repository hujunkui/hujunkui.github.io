---
title: nacos
date: 2020-09-22 15:35:12
tags:
- spring cloud
- nacos
comment:
password: 
categories:
- spring cloud
- nacos
cover: 
---

#### nacos 
nacos 启动报错

```bash
org.springframework.context.ApplicationContextException: Unable to start web server; nested exception is org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:156)
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:544)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:141)
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:744)
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:391)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:312)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1215)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1204)
        at com.alibaba.nacos.Nacos.main(Nacos.java:35)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:498)
        at org.springframework.boot.loader.MainMethodRunner.run(MainMethodRunner.java:49)
        at org.springframework.boot.loader.Launcher.launch(Launcher.java:107)
        at org.springframework.boot.loader.Launcher.launch(Launcher.java:58)
        at org.springframework.boot.loader.PropertiesLauncher.main(PropertiesLauncher.java:467)
Caused by: org.springframework.boot.web.server.WebServerException: Unable to start embedded Tomcat
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.initialize(TomcatWebServer.java:124)
        at org.springframework.boot.web.embedded.tomcat.TomcatWebServer.<init>(TomcatWebServer.java:86)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getTomcatWebServer(TomcatServletWebServerFactory.java:416)
        at org.springframework.boot.web.embedded.tomcat.TomcatServletWebServerFactory.getWebServer(TomcatServletWebServerFactory.java:180)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.createWebServer(ServletWebServerApplicationContext.java:180)
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.onRefresh(ServletWebServerApplicationContext.java:153)
        ... 16 common frames omitted
```



nacos 默认以集群模式启动

以单机模式启动

```bash
.\startup.cmd -m standalone
```

