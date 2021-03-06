---
title: Changelogs
description: Evolution of Sophie
published: 1
date: 2019-12-14T16:57:51.741Z
tags: 
---

## Sophie v2.0
> :warning: Under heavy development
{.is-warning}

### General changes
- Now Sophie checks admin rights to make sure the user has  rights to perform the action. For example, if the user doesn't have permission to ban users, they cannot use `/ban` command
- Sophie's help moved to the https://wiki.sophiebot.gq, help module was removed
- Sudo users were removed and converted to operators
- Global bans were removed
- Fixed issue when the command can be recognized not on the first line of the message
- Added [Imports/exports feature](/imports_exports)
- Added [stickers module](/stickers)

### [Notes](/notes)
- Support saving inline URL buttons from other bots
- Encryption method was changed to default MongoDB's one, it makes the decryption process faster and simpler
- Improved support for saving already formatted messages (Telegram X issue fixed)
- Implemented cashtags instead of old note settings, for example, instead of `[format:html]` you have to `%PARSEMODE_HTML`, old parsing settings left for backward compatibility
- Forbidden to save blank notes
- Implemented `/search` command to do a text search query in notes
- Implemented sorting by note name in `/notes` command feature
- Now after user press buttonnote but he blocked/never talked with bot, Sophie save state and after writing /start by user, she will send note
- Minor strings changes
- 'buttonnote' now will redirect in Sophie's PM instead of trying PM you first.

### [Federations](/feds) TODO
- Sophie now can ban users which she couldn't get
- Implemented `/importfbans` command
- Added JSON and CSV support for `/exportfbans`
- Added timestamp for every federation ban

### [Misc](/misc)
- `/stats` are now allowed only for operators
- `/runs` can be disabled for now

### [Restrictions](/restriction)
- Added silent commands for bans, mutes and kicking, like `/skick` or `/sban`
- Now after kicking or banning Sophie will delete 'Sophie removed X' service message

### [Greetings](/greetings)
- Module was fully rewrited
- `/setwelcome` now doesn't require note with welcome message in
- Now to disable welcome you have to use `/turnwelcome off`
- Updated welcome security: added security levels (button, math), old '1 click to unmute' method now named as 'button'.
- Added security note with which user will be propmted to validate his status in bot's PM.
- Now if Welcome Security is enabled, Sophie won't send welcome message in chat, but she will send in user's PM after they proved them as human.
- Added /welcomemute feature

### [Languages](/languages)
- Many improvements and fixes

### [Connections](/connections)
- Many improvements and fixes
- Added `/allowusersconnect` to disallow users to connect to chat (admins will be able to connect to the chat)
- If user hasn't started dialog with Sophie, but connected to the chat directly, after starting bot Sophie will reply with the 'connected successfully' message

### Errors reporting and crashlytics
- Sophie is now using sentry.io as crashlytics storage
- Removed the raw crash files feature

### Code changes
- Mainly we focus to support GNU/Linux OS or Docker, but Sophie may work on other OSs too.
- Bot config file changed to YAML
- Removed support of Telethon as commands register
- Sophie is now fully modular, modules ain't depending on each other
- Migrated from MongoDB Pymongo to MongoDB Motor
- Added apscheduller support
- Components were removed
- Dockerfile base image was changed to an Alpine instead of Ubuntu
- Translations were converted to YAML files instead of JSON
- Logging changed to a loguru library
- Introduced own API (Beta)

And tons of other edits and fixes