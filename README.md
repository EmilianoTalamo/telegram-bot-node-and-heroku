# Telegram Bot coded in NodeJS hosted at Heroku
Sample files to run a Telegram Bot with Heroku without [dyno sleeping](https://blog.heroku.com/app_sleeping_on_heroku).

## Requirements

* [NodeJS (and npm)](https://nodejs.org/en/)
* [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
* [node-telegram-bot-api](https://github.com/yagop/node-telegram-bot-api)
* [Bot token](https://web.telegram.org/#/im?p=@BotFather)

## References

* [Heroku NodeJS Documentation](https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction)
* [node-telegram-bot-api Documentation](https://github.com/yagop/node-telegram-bot-api/blob/master/doc/usage.md)

---

Make sure to run `npm install` before commiting your bot to Heroku.

---

## Prevent Dyno sleeping

By default, Heroku apps sleep after 1 hour of inactivity. This can be prevented by running the app as a worker dyno instead of a web dyno. This is already set on the Procfile, but make sure this is also true on your dashboard.

1. Go to your [Heroku dashboard]

2. Resources tab

![Resources Tab](https://i.imgur.com/vFMtJnN.jpg)

3. Check worker, uncheck web (if it's checked)

![Check worker, uncheck web](https://i.imgur.com/LxpbJlN.jpg)
