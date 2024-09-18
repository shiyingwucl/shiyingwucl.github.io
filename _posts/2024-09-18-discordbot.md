---
layout: post
title: Discord bot(working with api in python)
---

draft: resource [used](https://discordpy.readthedocs.io/en/stable/quickstart.html)

- learning api with discord bot in python

- api: application programming interface

- using the discord.py library

- bot design

- .env file

- token to communicate with discord api

## Understanding code

## Managing intents

```python

import discord
#asychronous, "callback" style(function called when something happens, i.e when bot detects that a user had sent a message) 

intents = discord.Intents.default()
intents.message_content = True
# sets intent.message_content to true so that discord bot can read messages

client = discord.Client(intents=intents)
# connection to discord?
```

```python
# discord.py uses asynchronous callback

@client.event # decorator 
async def on_ready(): 
    # "on_ready()" is an event that is called when the discord bot is online and logged in 
    print(f'We have logged in as {client.user}')

@client.event
async def on_message(message):
    # "on_message()" is called when discord detects a message
    if message.author ==client.user: 
        # checks if the message is from the bot itself
        return 
        # returns nothing (this is to stop bot from replying to its own)
    if message.content.startswith("!hello"):
        await message.channel.send("Hi!")

client.run("token") 
# this is needed to make the connection between the discord and the program
```
