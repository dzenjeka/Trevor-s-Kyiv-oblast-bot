# 🚨 Тривога | Київщина — Telegram bot

Бот перевіряє API alerts.in.ua та автоматично публікує в Telegram-канал:

- 🚨 початок повітряної тривоги в Київській області;
- 🟢 відбій, коли в області більше немає активної повітряної тривоги.

## Що потрібно перед запуском

1. Додати Telegram-бота адміністратором каналу `@Trevoga_Kiev_oblast` з правом публікувати повідомлення.
2. Отримати персональний API token на https://devs.alerts.in.ua/
3. На Render додати:
   - `TELEGRAM_BOT_TOKEN` — новий токен бота;
   - `ALERTS_API_TOKEN` — токен alerts.in.ua.
4. Запустити як Render Background Worker.

## Render

Build Command:
`pip install -r requirements.txt`

Start Command:
`python main.py`

Polling:
`30` секунд = 2 запити/хвилину, що нижче жорсткого ліміту API.

## Безпека

Не записуйте Telegram Bot Token або ALERTS API token у код, GitHub чи README.
