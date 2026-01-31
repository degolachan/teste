import discord
from discord.ext import commands

TOKEN = "MTQ2NjkzMjI1MjczODA2NDU4NQ.Gt6XOs.b1OUJgCLZkUCIP1sVR4Ca_-lIZ7_8lBJ6uTibQ"
VOICE_CHANNEL_ID = 1466943916849758432  # ID do canal de voz

intents = discord.Intents.default()
bot = commands.Bot(command_prefix="!", intents=intents)

@bot.event
async def on_ready():
    print(f"✅ Bot online como {bot.user}")

    channel = bot.get_channel(VOICE_CHANNEL_ID)
    if channel and isinstance(channel, discord.VoiceChannel):
        await channel.connect()
        print("🎧 Bot entrou na call!")
    else:
        print("❌ Canal de voz não encontrado")

bot.run(TOKEN)
