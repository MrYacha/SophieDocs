---
title: Changelogs
description: Evolution of Sophie
published: 1
date: 2019-11-06T20:29:27.859Z
tags: 
---

## Sophie v2.0
> :warning: Work in progress...
{.is-warning}

### General changes
- Now Sophie checks admin rights to make sure he has the rights to perform this action, for example, if user don't have permission to ban users he cannot use the `/ban` command
- Sophie's help moved to the https://wiki-sophie.orangefox.tech, help module was removed
- SUDO users were removed and converted to operators
- Global bans were removed
- Fixed issue when command can be recognized not on first line of message

### Notes
- Support saving inline URL buttons from other bots
- Encryption method was changed to default MongoDB's one, it makes the decryption process faster and simpler
- Improved support for saving already formatted messages (Telegram X issue fixed)
- Implemented cashtags instead of old note settings, for example, instead of `[format:html]` you have to `$FORMAT_HTML`, old parsing settings left for backward compatibility
- Markdown migrated to the botapi version, for example, instead of `**bold**` you have to `*bold*`
- Forbidden to save blank notes
- Minor strings changes

### Federations
- Sophie now can ban users which she could not get
- Implemented `/importfbans` command
- Added JSON and CSV support for `/exportfbans`
- Added timestamp for every federation ban

### Misc
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
- Removed raw crash files feature
- Added random strings to the crash message

### Code changes
- Only GNU/Linux OS are supported to run Sophie, otherwise, use Docker
- Bot config file changed to YAML
- Removed support of Telethon as commands register
- Sophie is now fully modular, modules independent of one another
- Migrated from MongoDB Pymongo to MongoDB Motor
- Added apscheduller support
- Components were removed
- Dockerfile base image was changed to an Alpine instead of Ubuntu
- Translations was converted to YAML files instead of JSON
- Logging changed to a loguru library
- Introduced own API (Beta)

And tons of other edits and fixes