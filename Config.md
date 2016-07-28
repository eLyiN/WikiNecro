Each of the following files are populated at different stages of the bots runtime.

# Config.json
## Location
#### DefaultAltitude (Value)
Altitude that the bot starts at. Not advised to change this from the default as Niantic does not check altitude.

#### DefaultLatitude (Value)
Latitude that the bot starts at. Must be between -90 and 90 values.

#### Default Longitude (Value)
Longitude that the bot starts at. Must be between -180 and 180 values

#### WalkingSpeedInKilometerPerHour
Obvious walking speed in kilometers per hour

#### MaxTravelDistanceInMeters (Value)
In meters, how far the bot will travel in a radius from the original default location.

#### UseGPXPathing (Value)
When `UseGPXPathing` is set to `true`, the bot will walk to the first point in the GPX path defined by the value in `GPXFile` and traverse each point. By default the bot wanders around the radius defined in `MaxTravelDistanceInMeters`.

#### GPXFile
Only used when `UseGPXPathing` is set to TRUE
Path of the GPX file relative to the .exe file. Place the GPX file in the same directory as the exe

## Evolution
#### EvolveAllPokemonAboveIV (Value)
When `EvolveAllPokemonAboveIV` is set to `true`, any Pokemon that is above the **EvolveAboveIVValue** value will be evolved if there are enough candies.

#### EvolveAboveIVValue (Value)
Only when `EvolveAllPokemonAboveIV` is set to `true`
Value used to determine what IV Pokemon should be automatically evolved at.

#### EvolveAllPokemonWithEnoughCandy (Value)
When `EvolveAllPokemonWithEnoughCandy` is set to `true`, any Pokemon listed in the PokemonsToEvolve list will be evolved every 5 Pokestops limited by the number of Pokemon and candies you have. If this is not set, Pokemon will not be evolved based on this list criteria.

#### PokemonsToEvolve (List)
Only used if `EvolveAllPokemonWithEnoughCandy` is set to true.
Comma-seperated quote-wrapped list of Pokemon names that distinguish which Pokemon to automatically evolve if there are enough candies.

#### KeepPokemonsThatCanEvolve (Value)
When NecroBot determines how many Pokemon to transfer due to duplicates, it will create a count based on the number of candies the account has for that species compared to the number required to evolve.

For example, if the account has 5 Pidgeys (12 candies to evolve) and 24 candies, NecroBot will keep the top two Pidgeys and transfer the rest.

## Transferring
#### PrioritizeIVOverCP (Value)
When `PrioritizeIVOverCP` is set to `true`, the bot will sort by IV instead of CP when deciding which Pokemon to transfer out of a group of duplicate Pokemon. By default, the bot sorts by CP.

#### TransferDuplicatePokemon (Value)
When `TransferDuplicatePokemon` is set to `true`, any Pokemon that meets the below criteria is transferred:
* Total number of that Pokemon species in your inventory is greater than `KeepMinDuplicatePokemon`
* Below the `KeepMinIVPercentage` value
* Below the `KeepMinCP` value
* Is not listed in your `PokemonsNotToTransfer` list

Note that any of the first three criteria are global values and they CAN be overwritten by the Pokemon-specific settings in the `PokemonsTransferFilter` list.

#### KeepMinDuplicatePokemon (Value)
NOTE: Only used if `TransferDuplicatePokemon` is set to `true`
This is a global setting that applies to any Pokemon that has not been overridden by an entry in the `PokemonsTransferFilter` list.

This value specifies how many duplicates of each Pokemon to keep when deciding what Pokemon to transfer. This number can be Pokemon-specific by creating an entry in the `PokemonsTransferFilter` list. A Pokemon can also be excluded from transfer with the `PokemonsNotToTransfer` list.

#### KeepMinIVPercentage (Value)
NOTE: Only used if `TransferDuplicatePokemon` is set to `true`
This is a global setting that applies to any Pokemon that has not been overridden by an entry in the `PokemonsTransferFilter` list.

This value specifies that a Pokemon that has an IV higher than this value will not be transferred. This number can be Pokemon-specific by creating an entry in the `PokemonsTransferFilter` list. A Pokemon can also be excluded from transfer with the `PokemonsNotToTransfer` list.

#### KeepMinCP (Value)
NOTE: Only used if `TransferDuplicatePokemon` is set to `true`
This is a global setting that applies to any Pokemon that has not been overridden by an entry in the `PokemonsTransferFilter` list.

This value specifies that a Pokemon that has an CP higher than this value will not be transferred. This number can be Pokemon-specific by creating an entry in the `PokemonsTransferFilter` list. A Pokemon can also be excluded from transfer with the `PokemonsNotToTransfer` list.

#### PokemonsNotToTransfer (List)
Only used if `TransferDuplicatePokemon` is set to `true`
Comma-seperated quote-wrapped list of Pokemon names that distinguish what Pokemon to keep regardless of their IV or CP so that they are not transferred. Pokemon in this list should never be transferred by NecroBot.

## Catching
#### UsePokemonToNotCatchFilter (Value)
When `UsePokemonToNotCatchFilter` is set to `true`, any Pokemon listed in the `PokemonsToIgnore` list will be skipped when determining what Pokemon to catch.

#### PokemonsToIgnore (List)
Only used if `UsePokemonToNotCatchFilter` is set to `true`.
Comma-seperated quote-wrapped list of Pokemon names that distinguish what Pokemon to ignore when searching to catch.

## Recycling/Items
#### UseEggIncubators (Value)
Automatically incubates eggs in order that they are listed in the inventory when the bot first runs.

#### UseLuckyEggsWhileEvolving (Value)
When `UseLuckyEggsWhileEvolving` is set to `true`, NecroBot will hold-off on evolving Pokemon until there are enough evolutions to meet the value in `useLuckyEggsMinPokemonAmount` and then proceed to use a Lucky Egg before evolving them.
Before triggering the evolve step, the bot will use a lucky egg if one has not been used in the past 30 minutes.

#### UseLuckyEggsMinPokemonAmount (Value)
Value used when evolving to determine the number of evolutions needed to trigger a Lucky Egg use.

#### ItemRecycleFilter (List)
List of max values mapped to each Pokemon Go item. During the recycling stage, any item that is over the max count is recycled to meet the value. This is to prevent full inventories.

## Other
#### AmountOfPokemonToDisplayOnStart (Value)
Every 5 stops when the bot displays a list of the top CP/IV Pokemon in your inventory, this setting will change how many Pokemon to display.

#### AutoUpdate (Value)
NecroBot will detect if it needs to update if set to `true`

#### ConfigPath (Value)
Populated value by Necrobot that should not be modified by most users

#### DelayBetweenPokemonCatch (Value)
Delay in milliseconds between attempts to catch a Pokemon.

#### RenameAboveIv (Value)
When `RenameAboveIv` is set to `true`, any Pokemon above the value in `KeepMinIvPercentage` is renamed.

#### TranslationLanguageCode (Value)
Translation code for Necrobot. Supported values can be found in the config/translations folder.

#### WebSocketPort (Value)
Port used by NecroBot for potential GUI implementations. Should not be modified.

# Auth.json
#### AuthType (Value)
Set to `google` for Google
Set to `ptc` for Pokemon Trainer Club
By default the bot will prompt for which login if Auth.json does not exist

#### GoogleRefreshToken (Value)
Token used by Necro-Bot to connect to the Google account. Delete this entry if you wish to login with another user account.

#### PtcUsername (Value)
Pokemon Trainer Club username used when `AuthType` is set to `ptc`

#### PtcPassword (Value)
Pokemon Trainer Club username used when `AuthType` is set to `ptc`