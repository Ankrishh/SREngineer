---
title: "Api"
description: "Dynatrace API usage."
lead: "Dynatrace API usage."
date: 2021-04-05T11:47:08+12:00
lastmod: 2021-04-05T11:47:08+12:00
draft: false
images: []
menu: 
  dynatrace:
    parent: "doc-guide"
weight: 420
toc: true
---

## API

> [doc](https://www.dynatrace.com/support/help/shortlink/section-api)

- [Environment API](https://www.dynatrace.com/support/help/shortlink/env-api)
    - API v1
    - API v2 (new)

<br/>

- [Configuration API](https://www.dynatrace.com/support/help/shortlink/config-api)


## Generate Token

> [doc](https://www.dynatrace.com/support/help/shortlink/api-authentication#generate-a-token)

    Settings > Integration > Dynatrace API > Create Token

Create token with required permissions.



## Usage Examples:

[Authentication](https://www.dynatrace.com/support/help/shortlink/api-authentication)

cURL:

```
curl --request GET \
  --url https://xxxxxx.live.dynatrace.com/api/v1/config/clusterversion \
  --header 'Authorization: Api-Token dt0c01.SYUH34HHG76HG7YN.G3DFFPORX6BNDVFFM572RZM'
```

Wget:

```
wget --no-check-certificate --quiet \
  --method GET \
  --timeout=0 \
  --header 'relativetime: 6h' \
  --header 'Authorization: Api-Token dt0c01.SYUH34HHG76HG7YN.G3DFFPORX6BNDVFFM572RZM' \
   'https://xxxxxx.live.dynatrace.com/api/v1/problem/feed'

```

PowerShell:

```
$headers = New-Object "System.Collections.Generic.Dictionary[[String],[String]]"
$headers.Add("Authorization", "Api-Token dt0c01.SYUH34HHG76HG7YN.G3DFFPORX6BNDVFFM572RZM")

$response = Invoke-RestMethod 'https://xxxxxx.live.dynatrace.com/api/v1/problem/feed' -Method 'GET' -Headers $headers
```



