import os

import requests

from telegram import Bot

BOT_TOKEN = os.environ["BOT_TOKEN"]

CHAT_ID = os.environ["CHAT_ID"]

bot = Bot(token=BOT_TOKEN)

URLS = [
    "https://www.pokemoncenter.com/en-gb/category/trading-card-game"
]

def send_message(text):
    bot.send_message(chat_id=CHAT_ID, text=text)

https://github.com/Peaky-07/pokemon-center-uk-bot

            
if r.status_code == 200:
                send_message(
                    f"Pokemon Center UK check successful\n{url}"
                )
            
else:
                send_message(
                    f"Store check returned {r.status_code}"
                )

    
except Exception as e:
        send_message(f"Bot error: {e}")

if __name__ == "__main__":

    check_store()