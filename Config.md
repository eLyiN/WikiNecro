Each of the following files are populated at different stages of the bots runtime.

# Config.json
## Variables
### DefaultAltitude
Altitude that the bot starts at. No current reason to change this at the moment.


### DefaultLatitude
Latitude that the bot starts at. Must be between -90 and 90 values.


### Default Longitude
Longitude that the bot starts at. Must be between -180 and 180 values


### DelayBetweenPokemonCatch
Delay in milliseconds between attempts to catch a Pokemon.

### KeepPokemonsThatCanEvolve
When NecroBot determines how many Pokemon to transfer due to duplicates, it will create a count based on the number of candies the account has for that species compared to the number required to evolve.

For example, if the account has 5 Pidgeys (12 candies to evolve) and 24 candies, NecroBot will keep the top two Pidgeys and transfer the rest.

### TransferDuplicatePokemon
When **TransferDuplicatePokemon** is set to TRUE, any pokemon that meets the below criteria is transferred:
* Total number of that pokemon species in your inventory is greater than **KeepMinDuplicatePokemon**
* Below the **KeepMinIVPercentage** value
* Below the **KeepMinCP** value
* Is not listed in your **ConfigPokemonsToKeep.ini** config file


### EvolveAllPokemonWithEnoughCandy
When **EvolveAllPokemonWithEnoughCandy** is set to TRUE, any Pokemon listed in ConfigPokemonsToEvolve.ini file will be evolved.


### UsePokemonToNotCatchFilter
When **UsePokemonToNotCatchFilter** is set to TRUE, any Pokemon listed in the ConfigPokemonsToKeep.ini file will not be listed for transfers regardless of CP or IV.


### PrioritizeIVOverCP
When **PrioritizeIVOverCP** is set to TRUE, the bot will sort by IV instead of CP when deciding which Pokemon to transfer out of a group of duplicate pokemon. By default, the bot chooses the strongest CP values when sorting.


### MaxTravelDistanceInMeters
In meters, how far the bot will travel in a radius from the original default location.


### UseGPXPathing
When **UseGPXPathing** is set to TRUE, the bot will walk to the first point in the GPX path defined by the value in **GPXFile** and traverse each point. By default the bot wanders around.


### GPXFile
Only used when **UseGPXPathing** is set to TRUE
Path of the GPX file relative to the .exe file. Place the GPX file in the same directory as the exe.


### useLuckyEggsWhileEvolving
Before triggering the evolve step, the bot will use a lucky egg if one has not been used in the past 30 minutes.


### EvolveAllPokemonAboveIV
When **EvolveAllPokemonAboveIV** is set to TRUE, any Pokemon that is above the **EvolveAboveIVValue** will be evolved if there are enough candies.


### EvolveAboveIVValue
Only when **EvolveAllPokemonAboveIV** is set to TRUE
Value used to determine what IV Pokemon should be automatically evolved at.

### RenameAboveIv
When ***RenameAboveIv*** is set to TRUE, any Pokemon above the value in ***KeepMinIvPercentage*** is renamed.

### UseEggIncubators
Automatically incubates eggs in order that they are listed in the invetory when the bot first runs.
___

## Lists
### ItemRecycleFilter
List of max values mapped to each Pokemon Go item. During the recycling stage, any item that is over the max count is recycled to meet the value. This is to prevent full inventories.


### PokemonsToEvolve
Only used if **EvolveAllPokemonWithEnoughCandy** is set to true.
Newline seperated list of capitalized Pokemon names that distinguish which Pokemon to automatically evolve if there is enough candies.


### PokemonsNotToTransfer
Only used if **TransferDuplicatePokemon** is set to true.
Newline seperated list of capitalized Pokemon names that distinguish what Pokemon to keep regardless of their IV or CP so that they are not transferred.


### PokemonsToIgnore
Only used if **UsePokemonToNotCatchFilter** is set to true.
Newline seperated list of capitalized Pokemon names that distinguish what Pokemon to ignore when searching to catch.


# Auth.json
### AuthType
Set to **google** for Google
Set to **ptc** for Pokemon Trainer Club
By default the bot will try to login using google.

### GoogleRefreshToken
Token used by Necro-Bot to connect to the Google account. Delete this entry if you wish to login with another user account.

### PtcUsername
Pokemon Trainer Club username used when AuthType is set to **ptc**

### PtcPassword
Pokemon Trainer Club username used when AuthType is set to **ptc**
