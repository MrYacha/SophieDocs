---
title: API
description: Well, please just don't DDoS me
published: 1
date: 2019-12-02T13:55:55.373Z
tags: 
---

API avaible by https://api.sophiebot.gq/

> API not will available till Sophie v2.0 released
{.is-warning}


## Usage
TODO

## Avaible API methods

[REST API methods are avaible here](/dev/rest)

## Code examples
### Python
#### Get current stats
``` python
import request

url = "https://api.sophiebot.gq/"
data = requests.get(url=url + 'stats-json').json()
print(data)
```