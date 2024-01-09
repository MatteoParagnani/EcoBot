# EcoBot
import discord
import random
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='\\', intents=intents)

@bot.event
async def on_ready():
    print(f'Hai fatto l\'accesso come {bot.user}')

@bot.command()
async def ciao(ctx):
    await ctx.send(f'Ciao! Sono un bot {bot.user}!')
lista_pericoli = [
    "Plastics in the ocean decompose into small pieces, which fish then eat and end up in our stomachs.",
    “Some fish species could become extinct due to plastic in the ocean,”
    "Some animal species may become extinct because their habitat has been degraded"
]
lista_ricicli[
    
'To reuse polystyrene you can create many things, for example: boxes, frames or things like that.',
    'to reuse bottles you can create many things, for example: with very large bottles a shoe rack, a jar, a pencil holder or things like that.',
    'to reuse the transparent plastic trays, by cutting 4 pieces, gluing them and placing them on the phone with a special video, you can create holograms'


]


@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)

@bot.command()
async def pericoli(ctx, tot=1):

    for i in range(tot):
        await ctx.send(random.choice(lista_pericoli))
@bot.command()
async def ricicliamo(ctx, tot=1):
    for i in range(tot):
        await ctx.send(random.choice(lista_ricicli))

@bot.command()
async def aiuto(ctx):
    await ctx.send(f'pericoli, ricicliamo')

bot.run("INSERISCI QUI IL TUO TOKEN")
