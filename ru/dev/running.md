---
title: Running bot
description: 
published: 1
date: 2019-10-31T19:53:40.783Z
tags: 
---

Sophie can be doployed by 2 ways

## Docker Way  
### Requirements 
+ git
+ installed Docker
  
### Cloning this repo  
	git clone https://github.com/MrYacha/SophieBot  
### Setting config  
  
+ Go to SophieBot/data  
+ Rename bot_conf.yaml.example to bot_conf.yaml  
+ Open in text editor  
+ Set mongo_conn to "mongo-server"  
+ Set redis_conn to "redis-server"  
+ Set other configs as needed  
  
### Creating bridge  
	docker network create sophiebot-net  
### Running Redis and MongoDB  
	docker run -d --rm --name redis-server --network sophiebot-net redis:alpine
	docker run -d --rm --name mongo-server --network sophiebot-net mongo:latest
### Builda & start a Sophie  
	cd SophieBot
	docker build . -t sophie
	docker run -d -v /home/yacha/SophieBot/data/:/opt/sophie_bot/data --network sophiebot-net sophie   
  
## Manual way 
### Requirements 
+ GNU/Linux based OS
+ git
+ python3.8+ (with pip installed)
+ MongoDB (or MongoDB Atlas account)
+ Redis

### Cloning this repo  
	git clone https://github.com/MrYacha/SophieBot  
  
### Setting config  
  
+ Go to SophieBot/data  
+ Rename bot_conf.json.example to bot_conf.json  
+ Open in text editor  
+ Set configs as needed  
  
### Installing requirements  
	cd SophieBot
	sudo pip3.8 install -r requirements.txt
  
### Running  
  
	cd SophieBot
	python3.8 -m sophie_bot