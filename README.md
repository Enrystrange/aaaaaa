import discord
from discord.ext import commands
import os, random

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'Hai fatto l\'accesso come {bot.user}')

@bot.command()
async def animali(ctx):
    img_name = random.choice(os.listdir('img'))
    with open(f'img/{img_name}', 'rb') as f:
        picture = discord.File(f)
 
    await ctx.send(file=picture)
@bot.command()
async def animali(ctx):
    img_name = random.choice(os.listdir('img'))
    with open(f'img/{img_name}', 'rb') as f:
        picture = discord.File(f)
 
    await ctx.send(file=picture)

bot.run("MTE2MDUxODYzMzk5MTE4ODUzMw.Ge8fwG.i9OT34CY5_j-KenNLLKoxbgffftcFGD9YLhj_w")
