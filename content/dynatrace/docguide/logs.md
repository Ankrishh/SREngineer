---
title: "Logs"
description: "Dynatrace Log file locations"
lead: "Dynatrace Log file locations"
date: 2021-04-05T11:41:55+12:00
lastmod: 2021-04-05T11:41:55+12:00
draft: false
images: []
menu: 
  dynatrace:
    parent: "doc-guide"
weight: 070
toc: true
---

## OneAgent

[Windows](https://www.dynatrace.com/support/help/shortlink/oneagent-disk-requirements-windows):

    %ProgramData%\dynatrace\oneagent\log

[Linux](https://www.dynatrace.com/support/help/shortlink/oneagent-disk-requirements-linux):

    /var/log/dynatrace/oneagent/

Note: There will be one log folder per monitored technology. Check 'os' folder for agent connectivity logs.

## OneAgent plugins

Windows:

    %ProgramData%\dynatrace\oneagent\log\plugin

Linux:

    /opt/dynatrace/oneagent/log/plugin

## ActiveGate

[Windows](https://www.dynatrace.com/support/help/shortlink/sgw-files#directory-locations):

    %ProgramData%\dynatrace\gateway\log

[Linux](https://www.dynatrace.com/support/help/shortlink/sgw-files#directory-locations):

    /var/log/dynatrace/gateway

## ActiveGate plugins

Windows:

    %ProgramData%\dynatrace\gateway\remotepluginmodule\logs\
    %PROGRAMFILES%\dynatrace\remotepluginmodule\plugin_deployment\<plugin>\bin\logs

Linux:

    /var/lib/dynatrace/remotepluginmodule/log/remoteplugin/
    /opt/dynatrace/remotepluginmodule/plugin_deployment/<plugin>/bin/logs