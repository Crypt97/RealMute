# RealMute: A PocketMine-MP chat management plugin by Leo3418
RealMute is a PocketMine-MP chat management plugin with many extra features.  
Here is some information that helps you start using this plugin quickly. For advanced guide, please visit [RealMute Wiki](https://github.com/Leo3418/RealMute/wiki).

## Features
* Mute and unmute individual players in chat
* Keep muting players even if they quit and join server again
* Mute all players in chat
* Time-limited mute
* Block and mute(optional) players who flood the chat screen
* Block and mute(optional) players if they send any prohibited contents set by administrator
* Mute players if their message exceeds length limit set by administrator, or slice the message only
* An optional function to disallow muted players to use signs
* An optional function to block players' private messages alongside chat messages
* An optional function to block messages from devices **(requires API 2.0.0 and higher)** or IPs (for API 1.x) that muted players used
* An optional function to keep allowing OPs sending messages while all players are muted
* An optional function to notify muted players when they are sending messages
* See list of muted players and status of the plugin
* Time-limitedly mute players who are automatically muted by this plugin
* [API methods](https://github.com/Leo3418/RealMute/wiki/API-methods-guide) that allow your plugin work with RealMute

## Usage
* `/rmute <player> [time]` Mute a player, you can specify time (in minutes) to use time-limited mute
* `/runmute <player>` Unmute a player
* `/muteall` Mute all players
* `/unmuteall` Unmute all players
* `/realmute help <page>` View help
* `/realmute notify <on|off|fake>` Toggle notification to muted players, or show a fake chat message to muted players
* `/realmute muteop` Include/Exclude OPs from muting all players
* `/realmute wordmute` Turn on/off auto-muting players if they send banned words
* `/realmute banpm` Turn on/off blocking private messages from muted players
* `/realmute banspam` Turn on/off auto-muting players if they flood the chat screen
* `/realmute banlengthy <mute|slice|off>` Mute/Slice/Allow messages exceeding the length limit
* `/realmute bansign` Allow/Disallow muted players to use signs
* `/realmute mutedevice` **(API 2.0.0 and higher only)** Turn on/off muting players' devices alongside usernames
* `/realmute muteip` **(API 1.x only)** Turn on/off muting players' IPs alongside usernames
* `/realmute spamth <time>` Specify spam threshold in seconds (If players sends consecutive messages within this time interval, they will be blocked)
* `/realmute amtime <time>` Set time limit(in minutes) of auto-mute, set 0 to disable
* `/realmute length <number of characters>` Set length limit of chat messages, set 0 to disable
* `/realmute addword <word>` Add a keyword to banned word list
* `/realmute delword <word>` Delete a keyword from banned word list
* `/realmute status` View current status of this plugin
* `/realmute list` List muted players
* `/realmute word` Show the banned-word list
* `/realmute about` Show information about this plugin

### Notes
* **Note on muting/unmuting players:** Player name is not case-sensitive. If you are muting/unmuting an online player, you may only need to enter several beginning characters of the player's name instead of the full name (like "Leo" instead of "Leo3418").
* **Note on using commands beginning with `/realmute`:** You can use alias `/rmt` for faster operations. For instance, you can use `/rmt status` instead of `/realmute status`.
* **Description of fake message notification:** Muted players will see a fake chat message in their client when they send one, so they will think that their message is successfully sent. The message is still invisible to other players.
* **Note on adding keywords:** You can add an exclamation mark before the word if you want to match the whole word only. For example, if you add `!bo`, `boy` will not be blocked, but `bo y` will be blocked.

## Notice on downgrading from version 3.x
Because of changes of internal mechanisms, configuration files generated by v3.x are not fully compatible with v2.4.x-v2.7.4.  
If you want to downgrade RealMute from v3.x to v2.x, please make sure you use [v2.7.5](https://github.com/Leo3418/RealMute/releases/tag/v2.7.5) or v2.0.x-v2.3.x.  

## License
This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.  
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.  
You should have received a copy of the GNU General Public License along with this program. If not, click [here](http://www.gnu.org/licenses/).