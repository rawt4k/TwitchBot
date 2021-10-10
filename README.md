# How It Works

```js
 identity: {
    username: 'YOUR BOTS USERNAME',   <-- This is where you place the username that you gave the bot account
    password: 'YOUR BOT OAUTH TOKEN',   <-- This is where you place the OAUTH token for the bot..
  },
  channels:['YOUR TWITCH CHANNEL'],    <-- This is YOUR Twitch user handle.. make sure it matches exactly..
};
```

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
});
```
This is a basic command for the bot.. inside the `if(message ==='!command')` is where youll put the trigger for the command.. Under that is the client action and thats what the bot says once the command is run..


# How to add more commands
 ```js
client.on('chat', (channel, user, message, self) => {
  if(message === '!ExampleCMD') {     
    client.action('Ventispurr', 'This is what the bot will say when the command is run');
``` 
Just copy this code and keep changing the client action and the command trigger for every command :D



For any other questions you can join my [Discord](ventispurr.cool/discord) For help from me !
