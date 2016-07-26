## FAQ overview

* Every Pokemon I try to catch returns CatchFlee and I cannot claim any Pokestops.
* When I try to build the source code, I receive a "One or more projects were not loaded correctly" error
* How do I run multiple bots at once?
* How do launch the Google login process again?
* How does egg hatching work?
* How do I use Lucky Eggs before the bot evolves Pokemon?
* How can I use incense, lucky eggs, and incubators?
* How do I ignore to catch a Pokemon?
* Why is my bot recycling items?
* [My Bot is repeating DisplayHighestCP](https://github.com/NecronomiconCoding/NecroBot/wiki/_new#my-bot-is-repeating-displayhighestcp)
* [Why is this Bot a bit slower than others?](https://github.com/NecronomiconCoding/NecroBot/wiki/FaQ#why-is-this-bot-a-bit-slower-than-others)
* [What does IV mean?](https://github.com/NecronomiconCoding/NecroBot/wiki/FaQ#what-does-iv-mean)
* [Where can I find the change location?](https://github.com/NecronomiconCoding/NecroBot/wiki/FaQ#where-can-i-find-the-change-location)
* [How do I know which radius value to use?](https://github.com/NecronomiconCoding/NecroBot/wiki/FAQ#how-do-i-know-which-radius-value-to-use)


### Every Pokemon I try to catch returns CatchFlee and I cannot claim any Pokestops.
Your account has been softbanned because your account has travelled too far to too short of a time window. 
The length of the soft ban depends on the distance that you traveled which can be anywhere from 5 mins to 3 hours.
Check your new location every 30 minutes until you can successfully catch Pokemon again.

***
### When I try to build the source code, I receive a "One or more projects were not loaded correctly" error
You must download the Rocket API release ZIP file and extract it into the Necro-bot directory. Follow steps #2-4 again

***
### How do I run multiple bots at once?
Create different directories that each have their own installation and run each of their .exe

***
### How do launch the Google login process again?
Delete the GoogleAuth.ini file from the Configs directory. Also make sure that you are logged into the Google account in your default browser. 

***
### How does egg hatching work?
As long as you are under 20 kmph, the eggs will hatch automatically when they are ready to hatch. There is no indication in the bot to show hatches.
To incubate an egg, you must log into the app. The bot may auto-incubate eggs in the future.

***
### How do I use Lucky Eggs before the bot evolves Pokemon?
Set **useLuckyEggsWhileEvolving** to TRUE in the settings. By default, this is set to FALSE. 
***

### How can I use incense, lucky eggs, and incubators?
Open the app on your device with location turned off (to prevent a softban) and manually trigger the item. This may change in the future with a feature.

***
### How do I ignore to catch a Pokemon?
Set **UsePokemonToNotCatchFilter** to TRUE and add the Pokemon to your Config/ConfigPokemonsNotToCatch.ini file

***
### Why is my bot recycling items?
In order to prevent the inventory from getting too full, the bot will automatically recycle items based on the values defined in the Config/ConfigItemList.ini file.

***
### Why are some Pokemon not being transferred?
Any pokemon that meets the below criteria is transferred:
* Total number of that pokemon species in your invetory is greater than **KeepMinDuplicatePokemon**
* Below the **KeepMinIVPercentage** value
* Below the **KeepMinCP** value
* Is not listed in your **ConfigPokemonsToKeep.ini** config file

### My Bot is repeating DisplayHighestCP
One of your Config Files has a typo.

***
### Why is this Bot a bit slower than others?
We are using a Humanizer, doesnt spam the Servers & hopefully will help in a banwave

***
### What does IV mean?
[Here](https://www.reddit.com/r/TheSilphRoad/comments/4tzcmk/faq_on_ivs_info_megathread/) is a Reddit post that will explain it all.

***
### Where can I find the change location?
Right [here](https://github.com/NecronomiconCoding/NecroBot/wiki/Getting-Started#changing-the-location-of-the-bot).

***
### How do I know which radius value to use?
Visit https://www.freemaptools.com/radius-around-point.htm, this website will help you out!

### I receive a "Value of parameter must be between -90,0 and 90,0" error when running the bot
Change the delimiter for lat/long within the .gpx file or config file from **comma** to **period** or vice versa

***