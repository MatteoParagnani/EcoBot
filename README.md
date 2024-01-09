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
    "Le plastiche nell'oceano si decompongono in piccoli pezzi, che poi i pesci mangiano e arrivano fino al nostro stomaco.",
    "Alcune specie di pesci potrebbero estinguersi per via delle plastiche nell'oceano",
    "Alcune specie animali potrebbero estinguersi perché il loro habitat è stato degradato"
]
lista_ricicli[
    'Per riutilizzare il polistirene si possono creare molte cose, per esempio: scatole, cornici o cose del genere.',
    'per riutilizzare delle bottiglie si possono creare molte cose, per esmpio: con bottiglie molto grandi una scarpiera, un vasetto, un portamatite o cose del genere.',
    'per rutilizzare i vassoi di plastica trasparente, tagliando 4 trapezzi, incolandoli e mettendoli sul telefono con un video apposito si possono creare degli ologrammi'



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

bot.run("INSERISCI QUI IL TUO TOKEN")
