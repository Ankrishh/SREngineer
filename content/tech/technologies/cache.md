---
title: "Cache"
description: ""
lead: ""
date: 2021-04-10T23:46:18+12:00
lastmod: 2021-04-10T23:46:18+12:00
draft: true
images: []
menu: 
  tech:
    parent: "technologies"
weight: 040
toc: true
---

## [Memcached ](https://memcached.org/)

- Key-Value database
- All data stored in memory only - except swap

Metrics:

- Memory usage
- Cache usage - % of available memory used for Memcached
- Connections - Number of open connections
- Hits Vs Misses

[Dynatrace Memcached monitoring](https://www.dynatrace.com/support/help/shortlink/memcached-server-monitoring)

## [Varnish](https://varnish-cache.org/)

- Caching reverse proxy
- Exclusively focused on HTTP

Metrics:
- Hits Vs Misses
- Connections

[Dynatrace Varnish Monitoring](https://www.dynatrace.com/support/help/shortlink/monitor-varnish)
- [Custom metrics](https://github.com/Dynatrace/snippets/tree/master/technologies/varnish/monitor-varnish-cache)