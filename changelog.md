---
title: Changelogs
description: Evolution of Sophie
published: 1
date: 2019-11-20T19:48:10.771Z
tags: 
---

## Sophie v2.0
> :warning: Work in progress...
{.is-warning}

### General changes
- Now Sophie checks admin rights to make sure he has the rights to perform this action, for example, if the user doesn't have permission to ban users he cannot use the `/ban` command
- Sophie's help moved to the https://wiki.sophiebot.gq, help module was removed
- SUDO users were removed and converted to operators
- Global bans were removed
- Fixed issue when the command can be recognized not on the first line of the message
- Added [Imports / exports feature](imports_exports)
- Added [stickers module](stickers)

### [Notes](notes)
- Support saving inline URL buttons from other bots
- Encryption method was changed to default MongoDB's one, it makes the decryption process faster and simpler
- Improved support for saving already formatted messages (Telegram X issue fixed)
- Implemented cashtags instead of old note settings, for example, instead of `[format:html]` you have to `%FORMAT_HTML`, old parsing settings left for backward compatibility
- Forbidden to save blank notes
- Implemented `/search` command to-do a text search query in notes
- Implemented sorting by note name in `/notes` command feature
- Now after user press buttonnote but he blocked/never talked with bot, Sophie save state and after writing /start by user, she will send note
- Minor strings changes

### [Federations](feds)
- Sophie now can ban users which she could not get
- Implemented `/importfbans` command
- Added JSON and CSV support for `/exportfbans`
- Added timestamp for every federation ban

### [Misc](misc)
- `/stats` are now allowed only for operators
- `/runs` are now can be disabled

### Languages
- Many improvements and fixes

### Connections
- Many improvements and fixes
- Added `/allowusersconnect` to disallow users to connect to chat (admins will be able to connect to the chat)
- If user is not initialized dialog with Sophie but connected to the chat directly - after activating bot Sophie will reply with the 'connected successfully' message

### Errors reporting and crashlytics
- Sophie is now using sentry.io as crashlytics storage
- Removed the raw crash files feature

### Code changes
- Only GNU/Linux OS are supported to run Sophie, otherwise, use Docker
- Bot config file changed to YAML
- Removed support of Telethon as commands register
- Sophie is now fully modular, modules independent of one another
- Migrated from MongoDB Pymongo to MongoDB Motor
- Added apscheduller support
- Components were removed
- Dockerfile base image was changed to an Alpine instead of Ubuntu
- Translations were converted to YAML files instead of JSON
- Logging changed to a loguru library
- Introduced own API (Beta)

And tons of other edits and fixes