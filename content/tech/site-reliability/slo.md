---
title: "SLO"
description: "Service Level Objective"
lead: "Service Level Objective"
date: 2021-04-04T21:40:21+12:00
lastmod: 2021-04-04T21:40:21+12:00
draft: false
images: []
menu: 
  tech:
    parent: "site-reliability"
weight: 020
toc: true
---

## Service Level Agreement (SLA)

Before starting with SLO, let's look at a more familiar term - Service Level Agreement (SLA).

Service Level Agreement is a support agreement that's put down on paper when entering into contract with a vendor. A good example of SLA is the support timeframe a vendor promises when you buy their software. Some example SLAs:
- Critical impact - Help will be provided within 0-2 hours.
- High impact - Help will be provided within 2-6 hours.
- Medium impact - Help will be provided within 6-24 hours.
- Low impact - Help will be provided within 1-3 days.

## Service Level Objective (SLO)

### What is SLO?

Now lets take this concept to your website. When a user opens your website they expect it to load fast and without  errors. They also expect the same for transactions on the website.

This expectation of fast, error free experience can be thought of an SLA between you, the website owner & the user. In the web world, this expectation exists even when there are no written agreements, and if it's breached, users are more likely to switch to a competitor.

Say your website normally takes 2.5 seconds to load and you have an advertised SLA that says the website home page will load within 5 seconds. Any time the website load time goes above 5s, you agree to take action to fix the slowness and bring it under 5 seconds within 2 hours. 

The questions you must ask yourself here are:
 1. Will users be happy if you consistently meet your SLA requirement alone?
 2. Will they tolerate load time of 5 seconds for up to 2 hours and stay loyal? 

The likely answer you will find is that users start getting unhappy even before load time hits 5 seconds. So if that's the case, you need a point where you know beyond which users are starting to get unhappy - This point could be 3 seconds load time. Whatever that point is, that's your Service Level Objective or SLO for load time.

In short, SLO is the point beyond which users start getting unhappy with your service. The other way to think about SLO is, once you find out the point beyond which users start getting unhappy, you make it your objective to always stay above this unhappiness level - that is your Service Level Objective or SLO.

### Advertising SLOs

SLOs are expressed as a percentage and have a timeframe associated with it.

For above example, a SLO statement will look something like this - "99% of requests within a period of 4 weeks will have a load time of less than 3s". This is called a 99% SLO.

So in case of our example:
- SLA = Load time < 5s
- SLO = Load time < 3s

The key component of SLO calculation is the [Service Level Indicator (SLI)](/tech/site-reliability/sli).

### Types of SLOs

SLOs can be calculated for any metric that you think is a good indicator of user happiness. Examples:

- Availability SLO
- Latency SLO
- Error Rate SLO

<br/>

Read more about SLOs here in [Google SRE Book](https://sre.google/sre-book/service-level-objectives/)

<br/>

> Credits: [Google SRE](https://sre.google/)

> Highly recommended course for Site Reliability Engineers - [Coursera - Site Reliability Engineering: Measuring and Managing Reliability](https://www.coursera.org/learn/site-reliability-engineering-slos)

