---
title: Changelogs
description: Evolution of Sophie
published: 1
date: 2019-11-06T16:43:20.096Z
tags: 
---

## Sophie v2.0
> :warning: Work in progress...
{.is-warning}

### General changes
- Now Sophie check admin rights to make sure he has rights to perform this action, for example if user don't have permission to ban users he cannot use the `/ban` command.
- Sophie's help moved to the https://wiki-sophie.orangefox.tech, help module was removed.
- SUDO users was removed and converted to operators.
- Global bans was removed.

### Notes
- Support saving inline URL buttons from other bots.
- Encryption method was changed to default MongoDB's one, it make decryption process faster and simpler.
- Improved support for saving already formatted messages (Telegram X issue fixed).
- Implemented cashtags instead of old note settings, for example, instead of `[format:html]` you have to `$FORMAT_HTML`, old parsing settings leaved for backward compatibility.
- Markdown migrated to botapi version, for example, instead of `**bold**` you have to `*bold*`.
- Forbidden to save blank notes.
- Minor strings changes.

### Federations
- Sophie now can ban users which she could not get.
- Implemented `/importfbans` command.
- Added JSON and CSV support for `/exportfbans`.
- Added timestamp for every federation ban.

### Misc
- `/stats` now allowed only for operators.
- `/runs` now can be disabled.

### Languages
- Many improvements and fixes.

### Connections
- Many improvements and fixes
- Added `/allowusersconnect` to disallow users to connect to chat (admins will be able connect to chat).
- If user not initialized dialog with Sophie but connected to chat directly - after starting bot Sophie will reply the 'connected successfully' message.

### Error reporting and crashlytics
- Sophie is now using sentry.io as crashlytics storage.
- Removed raw crash files feature.
- Added random strings to crash message.

### Code changes
- Only GNU/Linux OS are supported to run Sophie, otherwise use Docker.
- Bot config file changed to YAML.
- Removed support of Telethon as commands register.
- Sophie now fully modular, modules now independent of one another.
- Migrated from MongoDB Pymongo to MongoDB Motor
- Added apscheduller support.
- Components was removed.
- Dockerfile base image was changed to a Alpine instead of Ubuntu.
- Translations was converted to a YAML files instead of JSON.
- Logging changed to a loguru library.
- Indroduced own API (Beta).

And tons of other edits and fixes