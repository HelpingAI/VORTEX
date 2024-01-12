# VortexGPT

VortexGPT provides free access to text and image generation models.

## Getting Started:

    python -m pip install -U VortexGPT

Join my [Discord server](https://discord.gg/hf99YvT8qX ) for live chat, support, or if you have any issues with this package.

## Sources:

| Model        | Website                                               |
| ------------ | ----------------------------------------------------- |
| gpt3         | [chat9.yqcloud.top](https://chat9.yqcloud.top/)       |
| gpt4         | [you.com](https://you.com/)                           |
| alpaca_7b    | [chatllama.baseten.co](https://chatllama.baseten.co/) |
| falcon_40b   | [gpt-gm.h2o.ai](https://gpt-gm.h2o.ai/)               |
| prodia       | [prodia.com](https://prodia.com/)                     |
| pollinations | [pollinations.ai](https://pollinations.ai/)           |
| more         | comming soon                                          |
## Support this repository:

-   🎉 **Join my Discord Server:** Chat with me and others. [Join here](https://discord.gg/hf99YvT8qX ):

[![DiscordWidget](https://discordapp.com/api/guilds/1076407776403787796/widget.png?style=banner2)](https://discord.gg/hf99YvT8qX)

## Examples:

### Text Completion:

**Async:**

```python
from VortexGPT import AsyncClient
from asyncio import run


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await AsyncClient.create_completion("MODEL", prompt)
            print(f"🤖: {resp}")
        except Exception as e:
            print(f"🤖: {e}")


run(main())
```

**Non-Async:**

```python
from VortexGPT import Client

while True:
    prompt = input("👦: ")
    try:
        resp = Client.create_completion("MODEL", prompt)
        print(f"🤖: {resp}")
    except Exception as e:
        print(f"🤖: {e}")
```

### Image Generation:

**Async:**

```python
from VortexGPT import AsyncClient
from PIL import Image
from io import BytesIO
from asyncio import run


async def main():
    while True:
        prompt = input("👦: ")
        try:
            resp = await AsyncClient.create_generation("MODEL", prompt)
            Image.open(BytesIO(resp)).show()
            print(f"🤖: Image shown.")
        except Exception as e:
            print(f"🤖: {e}")


run(main())
```

**Non-Async:**

```python
from VortexGPT import Client
from PIL import Image
from io import BytesIO

while True:
    prompt = input("👦: ")
    try:
        resp = Client.create_generation("MODEL", prompt)
        Image.open(BytesIO(resp)).show()
        print(f"🤖: Image shown.")
    except Exception as e:
        print(f"🤖: {e}")
```
