---
title: Greetings
description: 
published: 1
date: 2019-11-24T20:04:07.095Z
tags: 
---

## Available commands
#### General
- `/setwelcome` or `/savewelcome`: Set welcome
- `/turnwelcome (on/off)`: Disable/enabled welcomes in your chat
- `/welcome`: Shows current welcomes settings
- `/resetwelcome`: Reset welcomes settings
{.grid-list}
#### Welcome security
- `/welcomesecurity (level)`: Set welcome security level
- `/welcomesecurity (off/no/0)`: Disable welcome security
- `/setsecuritynote`: Customise the `"Please press button below to verify themself as human!"` text
- `/delsecuritynote`: Reset security text to defaults 
{.grid-list}
#### Welcome mutes
- `/welcomemute (time)`: Set welcome mute (no media) for X time
- `/welcomemute (off/no)`: Disable welcome mute
{.grid-list}
#### Purges
- `/cleanwelcome (on/off)`: Deletes old welcome messages and last one after 45 mintes
- `/cleanservice (on/off)`: Cleans service messages (user X joined)
{.grid-list}


## Settings images, gifs, videos or stickers as welcome
Saving attachments on welcome is same as saving notes with it, [read the notes help about it](/notes). But keep in mind what you have to replace `/save` to `/setwelcome`

## Addings buttons and variables to welcomes or security text
Buttons and variables syntax is same as [notes buttons and variables](/notes#notes-buttons-and-variables)

## Welcome security

### Avaible levels:
- `button`: Ask user to press "I'm not a bot" button
- `captcha`: Ask user to enter captcha
{.grid-list}

If welcome security is enabled, user will be welcomed with security text, if user successfully verify self as user, he/she will be welcomed also with welcome text in his PM (to prevent spamming in chat).

If user didn't verified self for 24 hours he/she will be kicked from chat.
### Example: