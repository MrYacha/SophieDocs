---
title: API
description: Well, please just don't DDoS me
published: 1
date: 2019-11-02T19:27:24.968Z
tags: 
---

API avaible by https://api-sophie.orangefox.tech/

> API not will available till Sophie v2.0 released
{.is-warning}


## Usage
TODO

## Avaible API methods

### Alive:
- `alive`: Will be answered `{'status': 'ok'}` if everything ok, else will be `{'status': 'no'}`
{.grid-list}

### Stats:
- `stats-web/` : Will be sended page with stats (WARNING: Text on page will be white)
- `stats-json/` : Will be answered JSON compability stats
{.grid-list}

INDEV STATUS

## Code examples
### Python
#### Get current stats
``` python
import request

url = "https://api-sophie.orangefox.tech/"
data = requests.get(url=url + 'stats-json').json()
print(data)
```