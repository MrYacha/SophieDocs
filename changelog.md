---
title: Changelogs
description: 
published: 1
date: 2019-11-06T16:17:28.428Z
tags: 
---

## Sophie v2.0
> :warning: Work in progress...
{.is-warning}

### General changes
- Now Sophie check user admin rights to make sure he has rights to perform this action, for example if user don't have permission to ban user he cannot use `/ban` command.
- Sophie's help moved to https://wiki-sophie.orangefox.tech and help module was removed.
- SUDO users was removed and converted to operators.
- Global bans was removed and out team focused on Federations.

### Notes
- Support saving inline URL buttons from other bots.
- Encryption method changed to default MongoDB, it make decrpytion process faster and simpler.
- Improved support of saving already formatted messages (Telegram X issue fixed).
- Implemented cashtags instead of old note settings, instead of `[format:html]` used `$FORMAT_HTML` and `$FORMAT_NONE`, old parse setting leaved for compability.
- Markdown migrated to default bots version, instead of `**bold**` now used `*bold*`.
- Now you can't save blank note.
- Minor strings changes.

### Federations
- Sophie now can ban users which she could not get.
- Added `/importfbans`.
- Added JSON and csv support for `/exportfbans`.
- Added timestamp for every federation ban.

### Misc
- `/stats` now allowed only for operators.
- `/runs` now can be disabled.

### Languages
- Many improvements and fixes.

### Connections
- Many improvements and fixes
- Added `/allowusersconnect` to disallow users to connect to chat (admins will be able connect to chat).
- If user not started the bot in his pm and connected to chat, after starting Sophie will show 'connected successfully' message.

### Error reporting and crashlytics
- Sophie now using sentry.io as crashlytics storage.
- Removed generation crash files feature.
- Added random strings to crash message.

### Code changes
- Only GNU/Linux OS supported to run Sophie, otherwise use Docker.
- Bot config was changed to YAML.
- Removed support of Telethon as commands register in our @decorator.
- Sophie now fully modular, modules now independent of one another.
- Fully migrated to MongoDB Motor and Aiogram libraries instead of MongoDB pymongo and Telethon.
- Added apscheduller support.
- Components was removed.
- Dockerfile was converted to Alpine instead of Ubuntu.
- Translations was converted to YAML files instead of JSON.
- Logging changed to loguru lib
- Indroduced own API (Beta)

And tonns of other edits and fixes