Welcome to guilded.py, a discord.py-esque asynchronous Python wrapper for the Guilded API. If you know discord.py, you know guilded.py.

## Documentation

In the works. Fortunately, if you've used discord.py before, you'll already have a head start.

## Basic Example
### Clint Example :
```py
import guilded

client = guilded.Client()

@client.event
async def on_ready():
    print('Ready')

@client.event
async def on_message(message):
    if message.author == client.user:
        return
    if message.content == 'ping':
        await message.channel.send('pong')

client.run('email', 'password')
```
### Bot Example :
```py
import guilded
from guilded.ext import commands

bot = commands.Bot(command_prefix='?')
   
@bot.command()
async def ping(ctx):
    await ctx.send('Pong!')

@bot.event
async def on_ready():
    print('Bot is ready!')
```

For more examples, see the examples directory in this repository.

## Support

Guilded.py has a support channel under its dedicated group for any questions you may have.

1. Join the [Guilded-API](https://community.guildedapi.com) server
2. Navigate to #library-list
3. Click on the guilded.py role and click "Add me to role"
4. You should see a new group pop up in your sidebar - you are now in the Guilded.py group
