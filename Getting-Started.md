# Getting Started
Note: You will need some basic Computer Experience.
Need help? Join the [Chat](https://github.com/NecronomiconCoding/NecroBot/wiki/Chat-&-Rules#chatting-using-discord)! The Issue Tracker is not for help!

***
## Installation & Configuration
1. Download and Install [Visual Studio 2015](https://go.microsoft.com/fwlink/?LinkId=691979&clcid=0x409).
2. Download from [releases](https://github.com/NecronomiconCoding/NecroBot/releases).
3. Open `Pokemon GO Rocket API.sln`.
4. On the right hand side, double click on `UserSettings.settings`.
5. Enter the DefaultLatitude and DefaultLongitude which can be found [here](http://mondeca.com/index.php/en/any-place-en).
6. Select Authtype: `Google` or `Ptc` for Pokémon Trainer Club.
7. If you've selected Ptc, enter the Username and Password of the Ptc Account.
8. Right click on `PokemonGo.RocketAPI.Console` and click on `Set as Startup Project`.
9. Press `CTRL + F5` and follow the instructions.
10. Have fun!

## Changing the Location of the Bot
1. Get a new latitude and longitude.
2. Delete `Coords.ini` from the folder `PokemonGo.RocketAPI.Console\bin\Debug\Configs`.
3. Change the value of `DefaultLatitude` and `DefaultLongitude`in `UserSettings.settings`.
4. Compile and run `CTRL + F5`.

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