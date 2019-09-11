import discord 
from discord.ext import commands
import asyncio
import random
import urllib.parse, urllib.request, re

TOKEN = ''
prefix = "-"
bot = commands.Bot (command_prefix=prefix)

@bot.command()
async def youtube(ctx, *, search):

    query_string = urllib.parse.urlencode({
        'search_query': search
    })
    htm_content = urllib.request.urlopen(
        'http://www.youtube.com/results?' + query_string
    )
    search_results = re.findall('href=\"\\/watch\\?v=(.{11})', htm_content.read().decode())
    await ctx.send('http://www.youtube.com/watch?v=' + search_results[0])
    
@bot.command()
async def coin(ctx):
    toss = random.randint(0, 1)
    if toss == 0:
        await ctx.send('Heads')
    if toss == 1:
        await ctx.send('Tails')
        
@bot.command()
async def echo(ctx, *, arg):
    await ctx.send(arg)
