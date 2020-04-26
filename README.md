# Uniborg

Pluggable [``asyncio``](https://docs.python.org/3/library/asyncio.html)
[Telegram](https://telegram.org) userbot based on
[Telethon](https://github.com/LonamiWebs/Telethon).

## installing

#### Deploy To Heroku - Click The Picture Below

[![Deploy](https://media.extratv.com/2016/07/11/rami-malek-1-510x600.jpg)](https://heroku.com/deploy)


#### Generate String Session - Click The Picture Below

[![Repl.it](https://telegra.ph/file/7450155c09b092a5c9d8b.png)](https://GenerateStringSession.SpEcHIDe.repl.run)


## Internals

The core features offered by the custom `TelegramClient` live under the
[`uniborg/`](https://github.com/SpEcHiDe/uniborg/tree/master/uniborg)
directory, with some utilities, enhancements, the `_core` plugin, and the `_inline_bot` plugin.


## [@SpEcHlDe](https://telegram.dog/ThankTelegram)

- Only two of the environment variables are mandatory.
- This is because of `telethon.errors.rpc_error_list.ApiIdPublishedFloodError`
    - `APP_ID`:   You can get this value from https://my.telegram.org
    - `API_HASH`:   You can get this value from https://my.telegram.org
- The userbot will work without setting the non-mandatory environment variables.
- Please report any issues to the support group: [@SpEcHlDe](https://t.me/joinchat/AHAujEjG4FBO-TH-NrVVbg)


## Design

The modular design of the project enhances your Telegram experience
through [plugins](https://github.com/SpEcHiDe/uniborg/tree/master/stdplugins)
which you can enable or disable on demand.

Each plugin gets the `borg`, `logger`, `Config`, `tgbot` magical
[variables](https://github.com/spechide/UniBorg/blob/488eff632e65103ba7017d4f52777d22ddd52ea2/uniborg/uniborg.py#L76-L80)
to ease their use. Thus creating a plugin as easy as adding
a new file under the plugin directory to do the job:

```python
# stdplugins/myplugin.py
from telethon import events
from uniborg.util import admin_cmd

@borg.on(admin_cmd(pattern="hi"))
async def handler(event):
    await event.reply("hey")
```


## Learning

Check out the already-mentioned [plugins](https://github.com/SpEcHiDe/UniBorg/tree/master/stdplugins) directory, or some third-party [plugins](https://telegram.dog/UniBorg) to learn how to write your own, and consider reading [Telethon's documentation](http://telethon.readthedocs.io/).


## CREDITS


Thanks to:

- [lonami](https://lonami.dev) for creating [Telethon](https://github.com/lonamiwebs/Telethon)
- [SpEcHlDe](https://telegram.dog/ThankTelegram) 
- [Dark-Princ3](https://github.com/Dark-Princ3) 



[![?](https://i.ytimg.com/vi/fAyE9eQ6FYc/maxresdefault.jpg)](https://telegra.ph/file/bc7f54780b3732c8c8265.mp4 "?")
