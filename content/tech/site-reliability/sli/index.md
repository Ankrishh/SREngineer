---
title: "SLI"
description: "Service Level Indicator"
lead: "Service Level Indicator"
date: 2021-04-04T22:03:50+12:00
lastmod: 2021-04-04T22:03:50+12:00
draft: false
images: []
menu: 
  tech:
    parent: "site-reliability"
weight: 030
toc: true
---

## What is SLI?

Continuing with our previous example, beyond a load time of 3 seconds users start getting unhappy. Based on this, we chose our SLO - "99% of requests within a period of 4 weeks will have a load time of less than 3s".

The next step now is to measure the load time of every request and plot it on a chart. For this we are going to use below values.

    # For a selected time point
    SLI = (Count of requests with load time < 3s / Count of all requests) * 100
    
    # For a given timeframe
    SLO = ((Sum of all SLI)/Count of data points) * 100

{{< img src="sli.png" alt="Rectangle" caption="<em>credit: adapted from Google SRE</em>" class="border-0" >}}


Generically speaking:

    SLI = Good Events/Valid Events

In our example:
- Good event = load time < 3s
- Valid event = Any successful load action

## Types of SLIs

Any measure that you think accurately conveys user experience can be used for an SLI. Some examples:
- Availability SLI = Can connect/Total connection requests
- Response time (latency) SLI = Requests faster than threshold/All requests
- Success rate SLI = All successful requests/All requests

<br/>

> Credits: [Google SRE](https://sre.google/)

> Highly recommended course for Site Reliability Engineers - [Coursera - Site Reliability Engineering: Measuring and Managing Reliability](https://www.coursera.org/learn/site-reliability-engineering-slos)



 

