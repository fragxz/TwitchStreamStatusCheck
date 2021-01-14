If you are currently looking at the Github Repository, have a look at: https://fragxz.github.io/TwitchStreamStatusCheck/ or https://twitch-stream-status-checker.fragxz.de/
The Repository does not include any files, instead Issues and FAQs will be tracked here.

# DEMO
On the following [Website](https://twitch-stream-status-checker.fragxz.de/) you will find a Demo, where you will find a few Streamer and their current online status. They are dynamic and change according to their current live status.

# FEATURES
* Check the status of a streamer very easily (online / offline)
* It is very easy to implement (only 3 lines of code needed)
* Automatically gets the OAUTH token after first script execution (condition: clientID and secret are provided)
* Automatically renews the OAUTH token (expires every 60 days)

# HOW-TO
[![TwitchStreamStatus PreviewThumbnail](https://img.youtube.com/vi/ewcw5N4RMGU/0.jpg)](https://www.youtube.com/watch?v=ewcw5N4RMGU)

# Implementation
```php
require('twitch_status_tool.php');
$yourChannelName = new StreamerStatus("YourChannelName");
$yourChannelNameStatus = $yourChannelName->returnLiveStatus(); // result: "online" or "offline" 
```

# Requirements
* PHP Version: at least v5.6 - but v7 and higher is recommended
* Server needs to have permissions to read and write to the config-File
* cURL needs to be enabled in the php.ini / allowed on the server

The Twitch Stream Status Tool uses an App Access Token and the Client credentials flow - for more informations refer to the documentation: https://dev.twitch.tv/docs/authentication#types-of-tokens

This script is based on the new Twitch API (2020). The previous Twitch API was v5 / KRAKEN (deprecated). 

# Where to get the Script?
[On Codester](https://www.codester.com/items/27144/twitch-status-tool-php-script?ref=Fragxz)
