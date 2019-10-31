---
title: API
description: 
published: 1
date: 2019-10-31T21:45:14.585Z
tags: 
---

API avaible by https://api-sophie.orangefox.tech/

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