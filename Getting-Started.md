# Getting Started
Note: You will need some basic Computer Experience.
Need help? Join the [Chat](https://github.com/NecronomiconCoding/NecroBot/wiki/Chat-&-Rules#chatting-using-discord)! The Issue Tracker is not for help!

***
## Installation & Configuration
1. Download the latest release [Release.zip](https://github.com/NecronomiconCoding/NecroBot/releases).
2. Unzip the downloaded file and open up the `PoGo.NecroBot.CLI.exe.config`.
3. Edit the DefaultLatitude and DefaultLongitude which can be found [here](http://mondeca.com/index.php/en/any-place-en) to fit your desired location.
4. Select your authentication type: `Google` or `Ptc` for Pokémon Trainer Club.
5. If you've selected Ptc, enter the Username and Password of the Ptc Account.
6. Edit the other available settings to your desire
7. Run the `PoGo.NecroBot.CLI.exe`
8. Profit.

***
## Working with the source code
1. Download and Install [Visual Studio 2015](https://go.microsoft.com/fwlink/?LinkId=691979&clcid=0x409).
2. Get the current source code from [Code](https://github.com/NecronomiconCoding/NecroBot/archive/master.zip).
3. Get the current version of the RocketAPI we use from [RocketAPI](https://github.com/FeroxRev/Pokemon-Go-Rocket-API/archive/master.zip)
4. Unzip the RocketAPI so the folder structure matches `NecroBot\FeroxRev\PokemonGo.RocketAPI\`
4. Open `Pokemon GO Rocket API.sln`.
5. On the right hand side, double click on `UserSettings.settings`.
6. Enter the DefaultLatitude and DefaultLongitude which can be found [here](http://mondeca.com/index.php/en/any-place-en).
7. Select Authtype: `Google` or `Ptc` for Pokémon Trainer Club.
8. If you've selected Ptc, enter the Username and Password of the Ptc Account.
9. Right click on `PokemonGo.RocketAPI.Console` and click on `Set as Startup Project`.
10. Press `CTRL + F5` and follow the instructions.
11. Have fun!

## Changing the Location of the Bot
1. Get a new latitude and longitude.
2. If your Bot is running, close it.
3. Change the value of `DefaultLatitude` and `DefaultLongitude`in your `PoGo.NecroBot.CLI.exe.config`
4. Run the `PoGo.NecroBot.CLI.exe`

## GPX Pathing Setup
1. Go to [WTracks](https://wtracks.appspot.com/).
2. Create your path by right clicking on the map. Use as many points as you'd like! It is recommended to have the path end near the beginning of the path so it can loop.
3. Save without changing default settings.
4. Remove the [highlighted block of data](http://i.imgur.com/Px6Ba22.png) from the .gpx file using NotePad++ or NotePad.
5. Save the .gpx wherever your .exe is.
6. In the config set `UseGPXPathing` to `True` and `GPXFile` to `X.gpx` where `X` is your filename.
7. Set your default coordinates near the start of your path to begin pathing.
8. Launch the program!

## Error Handling
**[...] Value of parameter must be between -90,0 and 90,0 [...]**
* Change the delimiter for lat/long within the .gpx file from **comma** to **period** or vice versa