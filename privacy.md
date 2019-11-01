---
title: Data privacy and security
description: Sophie - the Facebook opposite
published: 1
date: 2019-11-01T15:53:13.544Z
tags: 
---

Sophie respects your privacy, every part of Sophie is open-source.
Sophie team constantly improve privacy and security.

> We don't collect your privacy data
We don't save your messages or any info about your messages
{.is-info}

## Which data we saving

### Public user's data
- We collect first and last names, users ID, nicknames and first detect timestamp
- We need this data for fast finding the user by nickname (ex. if you typing /warn @someone)
- We never use this data to make user profiles, this data used only to make Sophie faster and independent from Telegram's requests.
- If user pm'ed to bot, Sophie will save his Telegram's language.

### Chat data
- Chat name, username and chat ID
- We caching chat admins (1 hour after last command)

We not logging messages count, message's text or authors! 

### Analytics
We logging only Sophie's general metrics as:
- speed
- counting of data types in all chats
- % of using features in chats
- number of new chats in 48 hours

### Crashlytics
Crashlytics significantly helping Sophie be stable. We trying log as less data as possible, we can log only:
- Crash traceback
- Raw update data which caused crash
	
**Raw update example:**
`{"message_id":172915,"from":{"id":483808054,"is_bot":false,"first_name":"Yacha","username":"MrYacha","language_code":"en"},"chat":{"id":-1001414865722,"title":"[paperplane] \/\/ your spam is your deathwish\/\/","type":"supergroup"},"date":1572372681,"text":"\/crash","entities":[{"offset":0,"length":6,"type":"bot_command"}]}`