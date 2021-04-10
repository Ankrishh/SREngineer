---
title: "Troubleshooting"
description: ""
lead: "Troubleshooting issues."
date: 2021-04-05T11:46:53+12:00
lastmod: 2021-04-05T11:46:53+12:00
draft: false
images: []
menu: 
  dynatrace:
    parent: "doc-guide"
weight: 360
toc: true
---

## OneAgent

### Disable OneAgent instrumentation

- Option A: Switch monitoring to Infrastructure mode and restart application processes
- Option B: Uninstall OneAgent and restart application processes

NOTE: Stopping OneAgent service does not prevent instrumentation - only prevents collection of monitoring data. 
Application processes will be instrumented again even if OneAgent service is not running. This is due to ldpreload in linux and OneAgentMon device in Windows

### Other instrumentation related issues

NOTE: To be used in conjunction with Dynatrace Support to troubleshoot issues related to OneAgent

    Settings > Server-side service monitoring > Deep monitoring > Troubleshooting


## Service

### Service not detected

Likely reasons:

- Technology related features not enabled under:
    
    ```
    Settings > Monitored technologies

    Settings > Server-side service monitoring > Deep monitoring > New OneAgent features
    ```

- Custom code 
  
  May need custom service detection

    ```
    Settings > Server-side service monitoring > Custom service detection
    ```


- Service Detection Tags not passed properly

    From [Transactions and services](https://www.dynatrace.com/support/help/shortlink/transactions-and-services-hub) documentation:
    > To provide you with a continuous view of service flows Dynatrace uses the following means to track transactions across tiers:
    >
    > - `x-dynatrace` header for HTTP requests
    >
    > - `dtdTraceTagInfo` custom property for Java-based messaging services
    >
    > - A unique key for message queues (based on message properties)

    Above conditions maybe not met.

### Service showing as 'Opaque Service'

Possible reason:
- Code level monitoring is not supported for the process technology & service is created from the view of calling processes.

## Process

### No Process Connections but Service Flow present

  Process connections are detected from tcp traffic - so a proxy in between can affect detection. Service Flow are detected from x-dynatrace headers, so proxy doesn't affect it.