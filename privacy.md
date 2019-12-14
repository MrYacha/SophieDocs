---
title: Data privacy and security
description: Sophie - the Facebook opposite
published: 1
date: 2019-12-14T16:46:59.463Z
tags: 
---

Sophie respects your privacy, every part of Sophie is open-source.
Sophie's team are constantly improving privacy and security.

> We don't collect your private data.
We don't save your messages or any other information about them.
{.is-info}

## Which data we are saving

### Public user's data
- First and Second names, User ID, Telegram username
- Telegram language 
- Timestamp of the date when Sophie had seen the user first time.

### Chat data
- Chat name, username, and Chat ID
- We are caching chat admins (1 hour after the last command)

We are **not** logging messages count, messages text or their authors! 

### Analytics
- Speed of long queries
- Counting of data types in all chats
- Percents of using features in chats
- Number of new chats in 48 hours

### Crashlytics
Crashlytics significantly helping Sophie to be stable. We  are trying to log as fewer data as possible. Currently we can log only:
- Crash traceback
- Raw update data which caused crash
    
**Raw update example:**
``` python
{
  "message_id": 12345,
  "from": {
    "id": 123456789,
    "is_bot": false,
    "first_name": "A user",
    "username": "JustTelegramUser",
    "language_code": "en"
  },
  "chat": {
    "id": -100123456789,
    "title": "Just a group",
    "type": "supergroup"
  },
  "date": 1572372681,
  "text": "\/command",
  "entities": [{
    "offset": 0,
    "length": 8,
    "type": "bot_command"
  }]
}
```