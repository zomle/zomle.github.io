For questions/issues contact `zomle` on Twitch or write to my protonmail.com address (same username)

## Available commands
### For everyone
| Command | Description |
|:------------|-------------:|
| `!elo` | Displays elo of current channel owner |
| `!elo [hotaname]` | Displays elo of the specified hota user (if the bot recognizes the username) |
| `!game` | Displays info about current game of the channel owner |
| `!oppelo` | Displays elo of the opponent in the current game (if any game is in progress) |

### For broadcasters/mods
| Command | Description |
|:------------|-------------:|
| `!game edit [template] (hotauser1) [color] [faction] [trade] (hotauser2) [color] [faction] [trade] ...` | This sets info for current game. Any parameter can be omitted. |

#### For example:
| Command | Description |
|:------------|-------------:|
| `!game edit jc` | will set the template to Jebus Cross, and leave everything else as is |
| `!game edit zsemle red fort` | will set zsemle to be fortress and red, and leave other info as is |
| `!game 6lm10 kifli cove +1500 blue zsemle red necro` | will set the template to 6lm10, kifli to Cove, Blue and the trade +1500, and zsemle red and necro (also infers -1500 trade) |

If there are only 2 players, the main player will be the channel owner, and "opp" will be the opponent.

Also, it is enough to set trade and color for only one of the players, the other will be inferred (automatically set to red/blue and the trade will be the negated of the provided value).
| Command | Description |
|:------------|-------------:|
| `!game zsemle red inf 500 opp strong` | will set zsemle to red, inferno, +500 gold, and the opponent to stronghold, blue (inferred), -500 gold (inferred) |


