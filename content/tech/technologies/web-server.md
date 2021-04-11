---
title: "Web Server"
description: ""
lead: ""
date: 2021-04-10T23:49:41+12:00
lastmod: 2021-04-10T23:49:41+12:00
draft: false
images: []
menu: 
  tech:
    parent: "technologies"
weight: 230
toc: true
---

## [Apache HTTP Server](https://httpd.apache.org/)

## [Apache Tomcat](https://tomcat.apache.org/index.html)
- Pure java HTTP web server
- http request > web container > java servlet
- stackoverflow - "You can also setup Apache and Tomcat to work together with Apache serving static content and forwarding the requests for dynamic content to Tomcat" (Tomcat can also be used as general purpose http server).
- More features compared to Jetty but also more complex

## [Jetty](https://www.eclipse.org/jetty/)

- Mostly used for machine to machine communications, usually within larger software frameworks
- Examples of products using Jetty - Apache ActiveMQ, Google App Engine, Hadoop etc
- Less features compared to tomcat but light weight

Metrics
- [JVM metrics](/tech/technologies/language/#java)
- Jetty web requests
- Requests
- Connections

[Dynatrace Jetty monitoring](https://www.dynatrace.com/news/blog/jetty-web-server-metrics/)

## [Microsoft IIS](https://www.iis.net/)

Structure:
- Site (www.mywebsite.com) 
    - Application1 (www.mywebsite.com\application1)
        - Virtual Directories - /images, /stylesheets, /templates
        - Application pool made of Worker Processes
    - Application2 (www.mywebsite.com\application2) 
        - Virtual Directories - /images, /stylesheets, /templates
        - Application pool made of Worker Processes

Web Request Path: Client (Chrome) > HTTP.sys > Worker Process (Application pool)

Terms:
- Modules - IIS extensions

Metrics:
- Process Metrics
- Process availability

## [Nginx](https://www.nginx.com/)

Metrics:
- Requests per second 
- Response time
- Active Connections
- States
- Accepted
- Wait/Idle - connection currently not sending or receiving
- Reading
- Handled
- Dropped
- Response Code - 4xx, 5xx