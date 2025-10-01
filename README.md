bot.py

import discord
from discord.ext import commands

TOKEN = "YOUR_DISCORD_BOT_TOKEN"

intents = discord.Intents.default()
bot = commands.Bot(command_prefix="!", intents=intents)

@bot.event
async def on_ready():
    print(f"Bot is online as {bot.user}")

@bot.command()
async def hello(ctx):
    await ctx.send("Hello, World! 👋")

bot.run(TOKEN)


pip install discord.py
