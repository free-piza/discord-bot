import discord 
from discord.ext import commands
import asyncio
import random
import urllib.parse, urllib.request, re

TOKEN = ''
prefix = "-"
bot = commands.Bot (command_prefix=prefix)

@bot.event 
async def on_ready():
    print('bot is online!')
    i = 1 
    while i == 1:
        await bot.change_presence(activity=discord.Game(name='|Counting Servers|'))
        await asyncio.sleep(10)
        await bot.change_presence(activity=discord.Game(name='|5 Servers|'))
        await asyncio.sleep(10)
        await bot.change_presence(activity=discord.Game(name='|Prefix = - |'))
        await asyncio.sleep(10)
    print('Logged in as')
    print(bot.user.name)
    print(bot.user.id)
    print('------')

@bot.event
async def on_member_join(member):
    channel_welcome = discord.utils.get(
        member.guild.text_channels, name='welcome')
    await channel_welcome.send("{0} has joined the server! Welcome!".format(member))
    
   
@bot.event
async def on_command_error(ctx, error):
    await ctx.send('This command does not exist! Please try ~help for a list of commands!')
    print (error)
