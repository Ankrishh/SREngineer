---
title: "Error Budgets"
description: ""
lead: ""
date: 2021-04-04T22:04:11+12:00
lastmod: 2021-04-04T22:04:11+12:00
draft: false
images: []
menu: 
  tech:
    parent: "site-reliability"
weight: 040
toc: true
---

## What is an Error Budget?

In our SLO section we saw Reliability targets. Error budget is its opposite. Error budget says how much unreliable a service can be without breaching SLO.

Reliability = 99% ==> Error Budget = 1%

Reliability = 99.1% ==> Error Budget = 0.1%

## Why Error Budget?

It's a well known fact that the biggest contributor to IT system outages are failed changes. These changes can be hardware or software changes like replacement, upgrade, fix etc. 

Changes are unavoidable and usually steps are in place to mitigate risks of change. But, even with all the mitigation steps, problems can sometimes creep into production - in these cases Error Budget tells us what's acceptable. It coveys us how much downtime is tolerable without making users unhappy and hurting business.

## Why have a reliability target AND an error budget?

Reliability target --> For end users

Error budget --> For developers & sysadmins (or DevOps)

Error budgets tell developers & sysadmins (or DevOps) how fast they can release features into production. If Error budget is unused, go for faster innovation but if Error budget is depleted pause all changes and focus on reliability. 

Error budgets incentivize engineers to make the system more reliable so that they can release faster.

<br/>

> Credits: [Google SRE](https://sre.google/)

> Highly recommended course for Site Reliability Engineers - [Coursera - Site Reliability Engineering: Measuring and Managing Reliability](https://www.coursera.org/learn/site-reliability-engineering-slos)
