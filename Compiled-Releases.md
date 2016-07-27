# Getting Started - Compiled Release Setup
Note: You will need some basic Computer Experience.
Need help? Join the [Chat](https://github.com/NecronomiconCoding/NecroBot/wiki/Chat-&-Rules#chatting-using-discord)! The Issue Tracker is not for help!

***
## Installation & Configuration

### Compiled release steps are recommended for any end-user who has no intention of modifying the source code.


### Using compiled release
1. Download the latest release [Release.zip](https://github.com/NecronomiconCoding/NecroBot/releases).
2. Unzip the downloaded files, run the program (PoGo.NecroBot.CLI.exe)
3. Choose "0" for Google Auth and "1" for PTC auth and hit enter   
4a. **Google auth**, Necro-Bot has copied your device code onto your clipboard. Paste your code (Ctrl+V) into the Google website that pops up in your default browser to authenticate  (if the website does not pop-up go to http://google.com/device)   
4b. **PTC auth**, Type your username and hit enter, then type your password and hit enter   
5. Close bot and edit .\Config\config.json with your desired settings   
 * More details on these settings can be found [here](https://github.com/NecronomiconCoding/NecroBot/wiki/Config)
6. Put your latitude and longitude values in the `DefaultLatitude` and `DefaultLongitude` variables 
 * You can find GPS coordinates [here](http://mondeca.com/index.php/en/any-place-en) to fit your desired location.
7. Save the config.json file
8. Run `PoGo.NecroBot.CLI.exe` again

## Changing the Location of the Bot
1. Get a new latitude and longitude.
2. If your Bot is running, close it.
3. Change the value of `DefaultLatitude` and `DefaultLongitude` in your `Config/config.json` file
4. Run the bot