const TelegramBot = require('node-telegram-bot-api');

// Create a bot that uses 'webhook' to get updates 
const bot = new TelegramBot(token, {
    webHook: {
        port: 3000,
        autoOpen: false
    }
});

bot.openWebHook();// open/start webhook when app starts 

// Set webhook url. Ex: https://example.com/bot(required)yourBotToken
bot.setWebHook(` https://example.com/botHKJHKJ8989-hkjhjkIHJHKklkk90907`);

bot.onText(/\/start/, (msg) => {
    bot.sendMessage(msg.chat.id,`🖐 Hey ${msg.chat.first_name}`);
});

bot.onText(/\/bye/, (msg) => {
    bot.sendMessage(msg.chat.id,`🖐 Hayir ${msg.chat.first_name}`);
    console.log('hey')
});
