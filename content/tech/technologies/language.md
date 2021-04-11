---
title: "Language"
description: "Programming Languages and metrics. "
lead: "Programming Languages and metrics."
date: 2021-04-10T23:47:31+12:00
lastmod: 2021-04-10T23:47:31+12:00
draft: false
images: []
menu: 
  tech:
    parent: "technologies"
weight: 170
toc: true
---

## Erlang
## Go
## IBM CICS
## Java

[Starting a JAVA Application](https://docs.oracle.com/javase/7/docs/technotes/tools/windows/java.html)
    `java [options] class [arguments]`
    `java [options] -jar file.jar [arguments]`
    
  Options:
  
  - `-Dproperty=value` - System property value
      - Similar to environment variables but only accessible by java process
      - eg: `java -Dcustom_key="custom_value" -jar file.jar`

  [1 JVM per Java application](https://stackoverflow.com/questions/5947207/is-there-one-jvm-per-java-application) - i.e a separate process per application

  
Metrics (JVM):

- Process Availability 
- Java Heap Usage (memory allocated per process)
- Garbage Collection Overhead
- How long each GC cycle takes
- How often does GC run
- Number of Active Threads 
- Response time 

[Dynatrace Java Monitoring](https://www.dynatrace.com/support/help/technology-support/application-software/java/)

## Microsoft .NET

## Microsoft ASP.NET

## Node.js

## PHP

## Python

## Ruby
