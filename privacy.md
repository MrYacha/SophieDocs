---
title: Data privacy and security
description: Sophie - the Facebook opposite
published: 1
date: 2019-11-22T19:48:22.008Z
tags: 
---

Sophie respects your privacy, every part of Sophie is open-source.
Sophie's team constantly improve privacy and security.

> We don't collect your private data.
We don't save your messages or any info about your messages.
{.is-info}

## Which data we are saving

### Public user's data
- User name, user ID, nickname
- Telegram language 
- First detected timestamp

### Chat data
- Chat name, username, and chat ID
- We caching chat admins (1 hour after the last command)

We are not logging messages count, messages text or authors! 

### Analytics
- Speed of long queries
- Counting of data types in all chats
- % of using features in chats
- Number of new chats in 48 hours

### Crashlytics
Crashlytics significantly helping Sophie be stable. We trying log as fewer data as possible, we can log only:
- Crash traceback
- Raw update data which caused crash
    
**Raw update example:**
``` python
{
  "message_id": 172915,
  "from": {
    "id": 483808054,
    "is_bot": false,
    "first_name": "Yacha",
    "username": "MrYacha",
    "language_code": "en"
  },
  "chat": {
    "id": -1001414865722,
    "title": "[paperplane] \/\/ your spam is your deathwish\/\/",
    "type": "supergroup"
  },
  "date": 1572372681,
  "text": "\/crash",
  "entities": [{
    "offset": 0,
    "length": 6,
    "type": "bot_command"
  }]
}
```