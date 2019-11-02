---
title: Data privacy and security
description: Sophie - the Facebook opposite
published: 1
date: 2019-11-02T19:39:22.024Z
tags: 
---

Sophie respects your privacy, every part of Sophie is open-source.
Sophie team constantly improve privacy and security.

> We don't collect your privacy data
We don't save your messages or any info about your messages
{.is-info}

## Which data we saving

### Public user's data
- user name, user ID, nickname
- Telegram language 
- First detected timestamp

### Chat data
- Chat name, username and chat ID
- We caching chat admins (1 hour after last command)

We are not logging messages count, messages text or authors! 

### Analytics
- speed of long queries
- counting of data types in all chats
- % of using features in chats
- number of new chats in 48 hours

### Crashlytics
Crashlytics significantly helping Sophie be stable. We trying log as less data as possible, we can log only:
- Crash traceback
- Raw update data which caused crash
	
**Raw update example:**
`{"message_id":172915,"from":{"id":483808054,"is_bot":false,"first_name":"Yacha","username":"MrYacha","language_code":"en"},"chat":{"id":-1001414865722,"title":"[paperplane] \/\/ your spam is your deathwish\/\/","type":"supergroup"},"date":1572372681,"text":"\/crash","entities":[{"offset":0,"length":6,"type":"bot_command"}]}`