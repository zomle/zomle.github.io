## zsemlebot info
For questions/issues contact `zomle` on Twitch or write to my `zomle` at `protonmail.com` address.  

It is possible to link your own Twitch and Hota users by yourself, see below.

## Available commands
### For everyone

|    Command |  Description |
|------------|--------------|
| !elo | Displays elo of the current channel owner |
| !elo [name] | Displays elo of the specified twitch/user (if the bot recognizes the username) |
| !game | Displays info about current game of the channel owner |
| !game [name] | Displays info about current game of the specified twitch/user (if the bot recognizes the username) |
| !opp | Displays elo of the opponent in the current game (if any game is in progress) |
| !rep | Displays reputation of current channel owner |
| !rep [name] | Displays reputation of the specified twitch/hota user (if the bot recognizes the username) |
| !streak | Displays win/loss streak of the current channel owner |
| !streak [name] | Displays win/loss streak of the specified twitch/hota user (if the bot recognizes the username) |
| !today | Displays ranked wins/losses of current date for the current channel owner. Game times are based on UTC time, so channel owner must set `timezone` (see below) for correct results. |
| !today [name] | Displays wins/losss of current date for the specified twitch/hota user (if the bot recognizes the username). Game times are based on UTC time. |
| !unlinkme [hotaname] | Deletes the link between the current twitch user and the hota user |

### For broadcasters

|    Command |  Description |
|------------|--------------|
| !joinme [twitchname] | This command must be used in `zomle`'s Twitch chat. Makes the bot join the channel. `twitchname` must be the broadcaster's own name (just for confirmation) |
| !leave [twitchname] | Makes the bot leave the channel. `twitchname` must be the broadcaster's own name (just for confirmation) |
| !zsemlebot enable [command] | Enables the specified command in the current channel. E.g. 'enable !today' |
| !zsemlebot disable [command] | Disables the specified command in the current channel. E.g. 'disable !game' |
| !zsemlebot set timezone [offset]| Sets the timezone that's used in !today command. Format: `utc[+-](hours)` or `utc[+-](hours):(mins)`. E.g.: `utc+2` or `utc-5:30`, etc. |
| !zsemlebot unset timezone | Unsets the timezone reverting it to it's default value (utc time) |

### For broadcasters/mods

| Command | Description |
|------------|-------------|
| !game edit [template] (hotauser1) [color] [faction] [trade] (hotauser2) [color] [faction] [trade] ... | This sets info for current game. Any parameter can be omitted. |

#### For example:

| Command | Description |
|------------|-------------|
| !game edit jc | will set the template to Jebus Cross, and leave everything else as is |
| !game edit zsemle red fort | will set zsemle to be fortress and red, and leave other info as is |
| !game edit 6lm10 kifli cove +1500 blue zsemle red necro | will set the template to 6lm10, kifli to Cove, Blue and the trade +1500, and zsemle red and necro (also infers -1500 trade) |

If there are only 2 players, the main player will be the channel owner, and "opp" will be the opponent.

Also, it is enough to set trade and color for only one of the players, the other will be inferred (automatically set to red/blue and the trade will be the negated of the provided value).

| Command | Description |
|------------|-------------|
| !game edit zsemle red inf 500 opp strong | will set zsemle to red, inferno, +500 gold, and the opponent to stronghold, blue (inferred), -500 gold (inferred) |

## Linking your Twitch and Hota users
### Steps
1. Join the Hota lobby
2. Message the `konyer` user in the Hota lobby: ![Message konyer](https://raw.githubusercontent.com/zomle/zomle.github.io/master/zsemlebot/scr_linkme1.png)
3. Send a message to `konyer`: `!linkme <twitch name>`. For example if your Twitch name is zomle, type `!linkme zomle`
4. The bot will respond with an authentication code, that will have to be used on Twitch: ![Verification code](https://raw.githubusercontent.com/zomle/zomle.github.io/master/zsemlebot/scr_linkme2.png)
5. Now log in to Twitch and join `zomle` user's Twitch chat: [https://www.twitch.tv/popout/zomle/chat](https://www.twitch.tv/popout/zomle/chat)
6. Send the authentication code in chat in the following format: `!linkme <auth code>`: ![Twitch message](https://raw.githubusercontent.com/zomle/zomle.github.io/master/zsemlebot/scr_linkme3.png)
7. Your Twitch user and Hota user should be linked now. The bot will send back a confirmation message.

## Removing link between your Twitch and Hota users
1. Log in to Twitch and join `zomle` user's Twitch chat: [https://www.twitch.tv/popout/zomle/chat](https://www.twitch.tv/popout/zomle/chat)
2. Send the !unlink command to chat in the following format: `!unlinkme <hota user>`. For example: `!unlinkme zsemle`
3. The bot will delete the link between the Twitch and the Hota user.
