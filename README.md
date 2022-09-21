---
title: Telegram Bot
description: An ExpressJS server with a Telegram bot
tags:
  - express
  - telegraf
  - typescript
---

# Telegram bot example

This example starts a [Telegram](https://telegram.org/) bot on an [ExpressJS](https://expressjs.com/) server.

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new?template=https%3A%2F%2Fgithub.com%2Frailwayapp%2Fexamples%2Ftree%2Fmaster%2Fexamples%2Ftelegram-bot&envs=TELEGRAM_BOT_TOKEN)


### Deploy on Render.com
* build command: `yarn install; yarn run build-on-render`
* start command: `yarn start`

The custom build command shouldn't be necessary but it is.  Also render.com temperamentally fails to find `tsc`.  rebuild and it finds it.

Render.com's zero-downtime deploy process means that when doing a new deploy it'll start a replacement server before stopping your existing one, and you'll have two servers trying to comm for the same bot.  Things will fail.  You can't turn off this process (at time of writing - sep 2022).  Crappy Workaround: Stop the deployed service before deploying a new one.


## ✨ Features

- Telegraf (library to interact with the Telegram bot API)
- Express
- TypeScript

## 💁‍♀️ How to use

- Install dependencies `yarn`
- Connect to your Railway project `railway link`
- Start the development server `railway run yarn dev`

## 📝 Notes

The server started launches a Telegram bot with a couple of basic commands. The code is located at `src/index.ts`.
