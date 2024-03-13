## zsemlebot info
For questions/issues contact `zomle` on Twitch or write to my `zomle` at `protonmail.com` address.

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
| !today | Displays ranked wins/losses of current date for the current channel owner |
| !today [name] | Displays wins/losss of current date for the specified twitch/hota user (if the bot recognizes the username) |
| !unlinkme [hotaname] | Deletes the link between the current twitch user and the hota user |

### For broadcasters

|    Command |  Description |
|------------|--------------|
| !joinme [twitchname] | Makes the bot join the channel. `twitchname` must be the broadcaster's own name (just for confirmation) |
| !leave [twitchname] | Makes the bot leave the channel. `twitchname` must be the broadcaster's own name (just for confirmation) |
| !zsemlebot enable [command] | Enables the specified command in the current channel. E.g. 'enable !today' |
| !zsemlebot disable [command] | Disables the specified command in the current channel. E.g. 'disable !game' |
| !zsemlebot set timezone [offset]| Sets the timezone that's used in !today command. Format: `utc\[+-](hours)` or `utc\[\+-](hours):(mins)`. E.g.: `utc+2` or `utc-5:30`, etc. |
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


