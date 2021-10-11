# How It Works

```js
 identity: {
    username: 'YOUR BOTS USERNAME',   <-- This is where you place the username that you gave the bot account
    password: 'YOUR BOT OAUTH TOKEN',   <-- This is where you place the OAUTH token for the bot..
  },
  channels:['YOUR TWITCH CHANNEL'],    <-- This is YOUR Twitch user handle.. make sure it matches exactly..
};
```

# How to get OAUTH Token?
Its pretty easy actually.. if you want an auto generated one you can use [This](https://twitchapps.com/tmi/) to get one auto generated.. just make sure you make a new twitch account for the bot before doing it.. Don't wanna have the bot being youself lol.


# How to know the bot started up?

```js
client.on('connected', (address, port) => {
  client.action('Ventispurr', 'Hi! VentispurrBot is connected');   
});
```
This is what the bot says on console startup.. its how you'll know the bot is connected to your chat

# How to make a command
```js
client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {   
    client.action('Ventispurr', 'This is what the bot will say when the command is run');
}
});
```
This is a basic command for the bot.. inside the `if(message ==='!command')` is where youll put the trigger for the command.. Under that is the client action and thats what the bot says once the command is run..


# How to add more commands
 ```js
client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {     
    client.action('Ventispurr', 'This is what the bot will say when the command is run');
    }
    });
``` 
Just copy this code and keep changing the client action and the command trigger for every command :D

# How do I make the bot start?
You can use the console of anything.. Like replit, VS Code.. or anything that you really.. just run the command `npm index.js` and you'll be good to go..

# Bot goes off once I close the code text editor
This is normal.. unless you're hosting it with a vps.. You can do it for free if you're using replit..
```js
const express = require('express')
const app = express();
const port = 3000

app.get('/', (req, res) => res.send('Ventispurr was here!!'))

app.listen(port, () =>
  console.log(`Your app is listening to http://localhost:${port}`)
); 
```
Just put this at the top of the index.js file and put a few enters at the top.. then run the `npm install express` command.. after that run `npm index.js` again and youll notice in replit that this has shown up now.

![Screenshot 2021-10-10 175910](https://user-images.githubusercontent.com/91895035/136714252-df20f46f-0786-4b4b-9daf-f601d0d25ca7.png)

Thats good if you see this.. Once you do head over to [Uptime Robot](https://uptimerobot.com/login?rt=https://uptimerobot.com/dashboard#) and create an account and then create a new monitor.. copy the link that replit shows and then go through the uptime robot promps. This will ping the replit every 5 minutes so the bot wont shut down.. be sure to stop it once you're done streaming though!!

# For more help
You can join the [Discord](https://ventispurr.cool/discord) to get help from me!

