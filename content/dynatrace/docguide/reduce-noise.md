---
title: "Reduce Noise"
description: "Reduce noisy exceptions & traffic."
lead: "Reduce noisy exceptions & traffic."
date: 2021-04-05T11:45:40+12:00
lastmod: 2021-04-05T11:45:40+12:00
draft: false
images: []
menu: 
  dynatrace:
    parent: "doc-guide"
weight: 300
toc: true
---

## Global level

    Settings > Server-side service monitoring > Deep monitoring
       > Exclude noisy and unnecessary exceptions.
       > Exclude specific incoming web request URLs.

## Service level

    Transactions & services > {Service} > Edit > Error detection > Ignore exceptions