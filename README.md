# lavabot
import os
import discord
import requests
import json


client = discord.Client()
my_secret = os.environ['TOKEN']
@client.event
async def on_ready():
    print('We have logged in as {0.user}'.format(client))

@client.event
async def on_message(message):
    if message.author == client.user:
        return
    if message.content.startswith('lava hello'):
        await message.channel.send('Hello!')
    
    if message.content.startswith('lava who is sathviks bedmate'):
        await message.channel.send('rithvik')
    
    if message.content.startswith('lava vikram'):
        await message.channel.send('FUCK OFF')
     
    if message.content.startswith('lava good night'):
        await message.channel.send('Good Night!! sleep well')
    if message.content.startswith('lava who are you'):
        await message.channel.send('I am shatanshu raj from patna')
    if message.content.startswith('lava who is namrathas bf'):
        await message.channel.send('Anish Paul')
    

client.run(my_secret)

