---
title: "Introduction"
description: "Introduction to Site Reliability Concepts"
lead: "Introduction to Site Reliability Concepts"
date: 2021-04-04T09:27:09+12:00
lastmod: 2021-04-04T09:27:09+12:00
draft: false
images: []
menu: 
  tech:
    parent: "site-reliability"
weight: 010
toc: true
---

> Credits: [Google SRE](https://sre.google/)

## What is Site Reliability?

You could argue that the core purpose of any website is to have a place where users can access information and/or services 24x7. So when users open your website they expect it to be available. **Site Reliability** is the practise that strives to ensure this user expectation is met.

## So lets make our website 100% reliable.

No. This is the wrong target. No website is 100% reliable. Period.

There are countless components that influence the ability to get your website onto a user's browser. Some of them under your control, like your webserver, application code etc and others that are not under your control, like internet connectivity, ISP etc. So the best path is to manage the controllable aspects and set user expectations.

These user expectations are your **reliability targets**.

## How do you arrive at a reliability target?

The reliability target depends on a number of factors like:
- How critical is your website
    
    A banking website could be considered highly critical while a community notice board somewhat less critical.

- How many competitors you have

    Can your failure to provide service lead customers to your competitors?

- Who is your target audience
 
    If your target audience are tech savvy, they are likely to be more forgiving.

- What is your innovation level

    If you are a highly innovative website & users understand this (like using a Beta version of software) they are likely to forgive reliability for innovative features.

- and more..

Once these factors are factored in, you must decide how much downtime is acceptable and this will give you your reliability target.

### Lets see some numbers:

> This measurement can be done for different timeframes like year, month, 28d (4 weeks), a week etc. 1 year is used here.

Total minutes in a year = 365 * 24 * 60 = 525,600

- 99% Reliability:

    Uptime = 99% of 525,600 = 520,344 minutes

    Downtime = 1 % of 525,600 = 5,256 minutes or 87.6 hours per year

- 99.9% Reliability

    Uptime = 99.9% of 525,600 = 525,074.4 minutes

    Downtime = 0.1 % of 525,600 = 525.6 minutes or 8.76 hours per year

- 99.99% Reliability

    Uptime = 99.99% of 525,600 = 525,547.44 minutes

    Downtime = 0.01 % of 525,600 = 52.56 minutes or 0.876 hours per year

As you can see, with each additional 9 in reliability, the acceptable downtime narrows drastically. The cost of maintaining reliability also increases with each additional 9, as you have to put more and more resources like load balancing, high availability servers, engineers and so on into maintaining the reliability.

## Where to start?

If you have never measured reliability for your website, a good place to start would be by measuring existing reliability. Once you measure it below are are some concepts that can help you determine the reliability you should aim for.
- [Service Level Objective (SLO)](/tech/site-reliability/slo)
- [Service Level Indicator (SLI)](/tech/site-reliability/sli)
- [Error budgets](/tech/site-reliability/error-budgets)

<br/>

> Highly recommended course for Site Reliability Engineers - [Coursera - Site Reliability Engineering: Measuring and Managing Reliability](https://www.coursera.org/learn/site-reliability-engineering-slos)





