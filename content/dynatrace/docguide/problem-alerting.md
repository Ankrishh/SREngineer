---
title: "Problems & Alerting"
description: "Auto problem detection with built-in Davis AI."
lead: "Auto problem detection with built-in Davis AI."
date: 2021-04-05T11:44:17+12:00
lastmod: 2021-04-05T11:44:17+12:00
draft: false
images: []
menu: 
  dynatrace:
    parent: "doc-guide"
weight: 160
toc: true
---

## Thresholds

Out of the box static & dynamic thresholds defined for every metric coming into Dynatrace. No manual threshold definition overhead or concern about not setting threshold for a metric.

[Static Thresholds](https://www.dynatrace.com/support/help/shortlink/problem-evaluation) for infrastructure monitoring.

[Dynamic Thresholds](https://www.dynatrace.com/support/help/shortlink/automated-baselining) for everything else.

    Dynatrace UI > Settings > Anomaly detection    

## [Problem Detection](https://www.dynatrace.com/support/help/shortlink/problems-hub)

Automatic problem detection with Davis AI.

[How problems are detected and analyzed](https://www.dynatrace.com/support/help/shortlink/problems-intro)

[How Davis detects the impact of a problem](https://www.dynatrace.com/support/help/shortlink/problem-impact-level)

## [Adjust Problem Detection](https://www.dynatrace.com/support/help/shortlink/problem-detection-sensitivity)

### Global level

    Settings > Anomaly Detection
        > Applications
        > Services
        > Database Services
        > Infrastructure
        > Plugin events

### Host Group level

    Hosts > {Host} > Properties > Host Group > Settings > Anomaly detection


### Host Level

    Hosts > {Host} > Settings > Anomaly detection

### Services Level

    Transactions & services > {Service} > Settings > Anomaly detection

## Custom Alerts

[Custom Alerts](https://www.dynatrace.com/support/help/shortlink/event-types-custom-alerts)

[Custom alerts: What you set is what you get](https://www.dynatrace.com/news/blog/custom-alerts-set-get/)

    Settings > Custom Alerts


## Alerting

2 steps:

1. Create an [Alerting Profile](https://www.dynatrace.com/support/help/shortlink/alerting-profiles)

Define what Problems affecting what entities qualify for an alert to be sent out to you.

    Dynatrace UI > Settings > Alerting > Alerting profile

2. Create a Problem Notification integration.

Define what channel you want to receive the alert

    Dynatrace UI > Settings > Integration > Problem notifications

Available integrations:

- [Ansible Tower](https://www.dynatrace.com/support/help/shortlink/ansible-tower)

- [Email](https://www.dynatrace.com/support/help/shortlink/email-notifications)

- [Jira](https://www.dynatrace.com/support/help/shortlink/jira)

- [Microsoft Teams](https://www.dynatrace.com/support/help/shortlink/set-up-msteams-integration)

- [Opsgenie](https://www.dynatrace.com/support/help/shortlink/opsgenie)

- [PagerDuty](https://www.dynatrace.com/support/help/shortlink/pagerduty)

- [ServiceNow](https://www.dynatrace.com/support/help/shortlink/servicenow)

- [Slack](https://www.dynatrace.com/support/help/shortlink/set-up-slack-integration)

- [Trello](https://www.dynatrace.com/support/help/shortlink/trello-integration)

- [VictorOps](https://www.dynatrace.com/support/help/shortlink/victorops)

- [Webhook](https://www.dynatrace.com/support/help/shortlink/webhook)

- [xMatters](https://www.dynatrace.com/support/help/shortlink/id_xmatters-integration)





