# api-catdiva
Специальный модуль для бота "Кошка Дива 2.0" использующий API https://nekos.life
Примечание: Скоро будет создан собственный сайт с API, это пока что временно

#Установка
'''
pip install catdiva
'''

#Использование
'''
import discord
from discord.ext import commands
from discord.utils import get

from random import randint, choice
import random
import asyncio
import catdiva

class Test(commands.Cog):
    def __init__(self, client):
        self.client = client
        self.cog_name= ["Тестовая команда"] 


    @commands.command(
        aliases = ['хент', 'hentai'],
        description='интересные gif',
        usage='hentai'
    )
    async def _хентай(self, ctx):
        if ctx.channel.is_nsfw():
            r = ['feet', 'yuri', 'trap', 'futanari', 'hololewd', 'lewdkemo',
            'solog', 'feetg', 'cum', 'erokemo', 'les', 'wallpaper', 'lewdk',
            'ngif', 'tickle', 'lewd', 'feed', 'gecg', 'eroyuri', 'eron',
            'cum_jpg', 'bj', 'nsfw_neko_gif', 'solo', 'kemonomimi', 'nsfw_avatar',
            'gasm', 'poke', 'anal', 'slap', 'hentai', 'avatar', 'erofeet', 'holo',
            'keta', 'blowjob', 'pussy', 'tits', 'holoero', 'lizard', 'pussy_jpg',
            'pwankg', 'classic', 'kuni', 'waifu', 'pat', '8ball', 'kiss', 'femdom',
            'neko', 'spank', 'cuddle', 'erok', 'fox_girl', 'boobs', 'random_hentai_gif',
            'smallboobs', 'hug', 'ero', 'smug', 'goose', 'baka', 'woof'
		    ]
            rnek = nekos.img(random.choice(r))
            emb = discord.Embed(color = discord.Color.red())
            emb.set_image(url = rnek)
            await ctx.send(embed = emb)
        else:
            msg = await ctx.send(embed = discord.Embed(description='Не думаю, что это подходящий канал для такого контента...', color=discord.Color.orange()))
            await ctx.message.add_reaction('🔞')
            await asyncio.sleep(5)
            await msg.delete()

def setup(client):
    client.add_cog(Test(client))                
'''

# Что может выводить модуль
- cat
- eightball
- fact
- img
- owoify
- textcat
- why