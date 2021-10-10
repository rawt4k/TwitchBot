# How It Works

```js
 identity: {
    username: 'YOUR BOTS USERNAME',   <-- This is where you place the username that you gave the bot account
    password: 'YOUR BOT OAUTH TOKEN',   <-- This is where you place the OAUTH token for the bot..
  },
  channels:['YOUR TWITCH CHANNEL'],    <-- This is YOUR Twitch user handle.. make sure it matches exactly..
};
```

# How to add Commands?

```js
client.on('connected', (address, port) => {
  client.action('Ventispurr', 'Hi! VentispurrBot is connected');   <-- This is what the bot says on console startup..
});

client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {     <-- This is the command trigger you want.. 
    client.action('Ventispurr', 'This is what the bot will say when the command is run');   <-- This is that will run once you say the command trigger
  }
});
```
just copy the ```js
client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {     
    client.action('Ventispurr', 'This is what the bot will say when the command is run');``` 
code and keep changing the client action and the command trigger for every command :D
