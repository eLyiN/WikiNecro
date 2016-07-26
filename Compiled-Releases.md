# Getting Started - Compiled Release Setup
Note: You will need some basic Computer Experience.
Need help? Join the [Chat](https://github.com/NecronomiconCoding/NecroBot/wiki/Chat-&-Rules#chatting-using-discord)! The Issue Tracker is not for help!

***
## Installation & Configuration

### Compiled release steps are recommended for any end-user who has no intention of modifying the source code.


### Using compiled release
1. Download the latest release [Release.zip](https://github.com/NecronomiconCoding/NecroBot/releases).
2. Unzip the downloaded files, run the program (PoGo.NecroBot.CLI.exe), close it.
3. Edit .\Config\auth.json
3. Edit AuthType to be "google" for Google, "ptc" for Ptc
4. Edit your password and username when choosing PTC login
5. Save the auth.json file
6. Edit .\Config\config.json with your desired settings
 * More details on these settings can be found [here](https://github.com/NecronomiconCoding/NecroBot/wiki/Config)
7. Put your latitude and longitude values in the `DefaultLatitude` and `DefaultLongitude` variables 
 * You can find GPS coordinates [here](http://mondeca.com/index.php/en/any-place-en) to fit your desired location.
8. Save the config.json file
9. Run `PoGo.NecroBot.CLI.exe` again
10. For "Google login", Necro-Bot has copied your device code onto your clipboard. Paste your code (Ctrl+V) into the Google website that pops up in your default browser to authenticate  (if the website does not pop-up go to http://google.com/device)
11. Click next and next again and Bot will start.

## Changing the Location of the Bot
1. Get a new latitude and longitude.
2. If your Bot is running, close it.
3. Change the value of `DefaultLatitude` and `DefaultLongitude` in your `Config/config.json` file
4. Run the bot