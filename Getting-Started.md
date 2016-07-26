# Getting Started
Note: You will need some basic Computer Experience.
Need help? Join the [Chat](https://github.com/NecronomiconCoding/NecroBot/wiki/Chat-&-Rules#chatting-using-discord)! The Issue Tracker is not for help!

***
## Installation & Configuration

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

### Using GitHub pull and repository
#### **Downloading necessary files**
Download and Install [Visual Studio 2015](https://go.microsoft.com/fwlink/?LinkId=691979&clcid=0x409).

#### Source code as zip-files
1. Get the current source code from [Code](https://github.com/NecronomiconCoding/NecroBot/archive/master.zip).
2. Get the current version of the RocketAPI we use from [RocketAPI](https://github.com/FeroxRev/Pokemon-Go-Rocket-API/archive/master.zip)
3. Unzip the source code for NecroBot
4. Unzip the RocketAPI so the folder structure matches `NecroBot\FeroxRev\PokemonGo.RocketAPI\`
	
#### Source code via git (faster, always up2date)
1. open your terminal (you should have [git for windows](https://git-for-windows.github.io) installed)
2. change to the folder where you want to clone the files to and type into terminal
3. `git clone --recursive https://github.com/NecronomiconCoding/NecroBot.git`
	
#### Setup
1. Open `NecroBot for Pokemon Go.sln`.
2. Right click on `PoGo.NecroBot.CLI` and click on `Set as Startup Project`.
3. Press `CTRL + F5` and close the window
4. Edit NecroBot\PoGo.NecroBot.CLI\bin\Debug\Config\auth.json
5. Edit AuthType to be "google" for Google, "ptc" for Ptc
6. Edit your password and username when choosing PTC login
7. Save the auth.json file
8. Edit NecroBot\PoGo.NecroBot.CLI\bin\Debug\Config\config.json with your desired settings
 * More details on these settings can be found [here](https://github.com/NecronomiconCoding/NecroBot/wiki/Config)
9. Put your latitude and longitude values in the `DefaultLatitude` and `DefaultLongitude` variables 
 * You can find GPS coordinates [here](http://mondeca.com/index.php/en/any-place-en) to fit your desired location.
10. Save the config.json file
11. Press `CTRL + F5` and follow the instructions.

**NOTE:** If PogoProtos is missing: Its in the packages folder, just right click the CLI -> Add Reference -> Browse (tab) -> Browse (button) -> go to the packages folder in the root directory and find the PogoProtos
***

## Changing the Location of the Bot
1. Get a new latitude and longitude.
2. If your Bot is running, close it.
3. Change the value of `DefaultLatitude` and `DefaultLongitude`
 * For Compiled (Release) installation, in your `Config/config.json` file
 * For Source code (Repo) installation, in your `NecroBot\PoGo.NecroBot.CLI\bin\Debug\Config\config.json` file
4. Run the bot

**Note:** Moving your account's location too far over a short period of time will place a soft-ban on your account depending on the distance traveled.

## GPX Pathing Setup
1. Go to [WTracks](https://wtracks.appspot.com/).
2. Create your path by right clicking on the map. Use as many points as you'd like! It is recommended to have the path end near the beginning of the path so it can loop.
3. Save without changing default settings.
4. Remove the [highlighted block of data](http://i.imgur.com/Px6Ba22.png) from the .gpx file using NotePad++ or NotePad.
5. Save the .gpx wherever your .exe is.
6. In the config set `UseGPXPathing` to `True` and `GPXFile` to `X.gpx` where `X` is your filename.
7. Set your default coordinates near the start of your path to begin pathing.
8. Launch the program!

Submitted GPX paths can be found [here](https://github.com/NecronomiconCoding/NecroBot/wiki/Locations-&-GPX-Route-Files).