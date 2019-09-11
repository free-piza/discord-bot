import discord 
from discord.ext import commands
import asyncio
import random
import urllib.parse, urllib.request, re

TOKEN = ''
prefix = "-"
bot = commands.Bot (command_prefix=prefix)

@bot.command()
async def DM(ctx, persontosendto: discord.Member, *, msg):
    allroles = []
    for role in ctx.author.roles:
        if role.id in allroles:
            await persontosendto.send(msg)
            await ctx.send(f"{ctx.author.mention} Message sent!")
            return
           
@bot.command()
async def SPAM(ctx):
    roles = ctx.author.roles
    list_variable = []
    if discord.utils.get(list_variable):
        await ctx.send('Stop Spamming Chat Or You Will Be Punished!! This Is Your Warning!!')
    else:
        await ctx.send('')

@bot.command()
async def kick(ctx, userName: discord.Member):
    roles = ctx.author.roles
    list_variable = ['']
    if discord.utils.get(list_variable):
        await userName.kick()
        print('CHAT BOT = "A user has been kicked"')
    else:
        await ctx.send('')
        
        @bot.command()
async def delete(ctx, amount : int):
    list_variable = ['']
    channel = ctx.message.channel
    messages = []
    if discord.utils.get(list_variable):
        async for message in ctx.channel.history(limit=int (amount)):
            messages.append(message)
        await ctx.message.channel.purge(limit=amount)
        await ctx.send('messages deleted')
        print('CHAT BOT = "message/s deleted"')
    else:
        await ctx.send('')
        
bot.run(TOKEN)
