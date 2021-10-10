# How It Works

```js
 identity: {
    username: 'YOUR BOTS USERNAME',   <-- This is where you place the username that you gave the bot account
    password: 'YOUR BOT OAUTH TOKEN',   <-- This is where you place the OAUTH token for the bot..
  },
  channels:['YOUR TWITCH CHANNEL'],    <-- This is YOUR Twitch user handle.. make sure it matches exactly..
};

# How to add Commands?


client.on('connected', (address, port) => {
  client.action('Ventispurr', 'Hi! VentispurrBot is connected');   <-- This is what the bot says on console startup..
});

client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {     <-- This is 
    client.action('Ventispurr', 'This is what the bot will say when the command is run');   <-
  }
});
