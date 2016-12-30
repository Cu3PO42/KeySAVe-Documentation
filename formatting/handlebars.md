# The Handlebars formatting plugin

The Handlebars plugin was created as an alternative to KeySAV2's formatting strings. It can generate arbitrary HTML and is very versatile and powerful.

You have the following settings:

  * A header that will be displayed over the dumping output
  * A handlebars template to format each Pokémon
  * The toggle to separate the boxes from each other
  * And a template that is used to generate the heading for each box.

{% raw %}

## Introduction to Handlebars

It is entirely impossible for me to cover every aspect of the Handlebars language, so I do recommend you take a look at the [official documentation](http://handlebarsjs.com), but I will give you a very quick rundown of the most basic features:

Your templates can contain arbitrary HTML that will be rendered. Any expression encased by two curly braces (`{{expresion}}`) will be evaluated in the context of the current object, in our case a Pokémon. It has the following properties that can be used as expressions:

## Properties

| Property | Meaning (if not self explanatory) |
|----------|-----------------------------------|
|`ec`|The encryption constant used to encrypt and decrypt the Pokémon. It's unique to each Pokémon.|
|`pid`|The Personality ID|
|`exp`|The Amount of Experience.|
|`evHp`||
|`evAtk`||
|`evDef`||
|`evSpAtk`||
|`evSpDef`||
|`evSpe`||
|`ivHp`||
|`ivAtk`||
|`ivDef`||
|`ivSpAtk`||
|`ivSpDef`||
|`ivSpe`||
|`contestStatCool`||
|`contestStatBeauty`||
|`contestStatCute`||
|`contestStatSmart`||
|`contestStatTough`||
|`contestStatSheen`||
|`markings`|The markers you can set in your PC on every Pokémon: circle, triangle, etc. This is a [bitfield](https://en.wikipedia.org/wiki/Bit_field) of width 8. From least significant to most significant, the bits represent the following markers (each bit is 1 if ther marker is set, otherwise 0): circle, triangle, square, heart, star, diamond.|
|`hpType`||
|`pkrsStrain`||
|`pkrsDuration`||
|`levelMet`||
|`otGender`||
|`ability`|The ID of the ability a Pokémon has.|
|`abilityNum`|The ability slot of the ability for the Pokémon.|
|`nature`||
|`species`||
|`heldItem`||
|`tid`|The TID as it would be shown by the game.|
|`sid`||
|`tid7`|The TID as used in Generation 6 and previous ones.|
|`tid7`|The TID as used in Generation 7.|
|`tsv`||
|`esv`||
|`move1`||
|`move2`||
|`move3`||
|`move4`||
|`move1Pp`|The total amount of PP for the move.|
|`move2Pp`||
|`move3Pp`||
|`move4Pp`||
|`move1Ppu`|The number of PP Ups that were used on this move.|
|`move2Ppu`||
|`move3Ppu`||
|`move4Ppu`||
|`eggMove1`||
|`eggMove2`||
|`eggMove3`||
|`eggMove4`||
|`ribbonSet1`|A bitfield representing some of the ribbons your Pokémon can have of width 16: from least significant to most significant (in Big-Endian): Kalos Champ, Champion, Sinnoh Champ, Best Friends, Training, Skillfull Battler, Expert Battler, Effort, Alert, Shock, Downcast, Careless, Relax, Snooze, Smile, Gorgeous.|
|`ribbonSet2`|Another bitfield of width 16 constituting ribbons: Royal, Gorgeous Royal, Artist, Footprint, Record, Legend, Country, National, Earth, World, Classic, Premier, Event, Birthday, Special, Souvenir. |
|`ribbonSet3`|A bitfield of width 8 representing the following ribbons: Wishing, Battle Champion, Regional Champion, World Champion, None, None, Hoenn Champion.|
|`ribbonSet4`|A bitfield of width 8 representing the following ribbons: Contest Star, Coolness Master, Beauty Master, Cuteness Master, Cleverness Master, Toughness Master.|
|`chk`|The checksum for the file. It is not invariant.|
|`otFriendship`||
|`otAffection`||
|`eggLocation`||
|`metLocation`||
|`ball`||
|`encounterType`||
|`gameVersion`||
|`countryID`||
|`regionID`||
|`dsregID`||
|`otLang`||
|`box`|The box this Pokémon was dumped from. [Zero-indexed](https://en.wikipedia.org/wiki/Zero-based_numbering).|
|`slot`|The slot in a box this Pokémon was found in. Imagine there being no 'line breaks' in the boxes, then this would be the index of the Pokémon. Zero-indexed.|
|`form`||
|`gender`|`0` represents male, `1` represents female, `2` is genderless.|
|`metDate`|The date the Pokémon was hatched or captured. Represented as an array of three values in JavaScript standard. The first element is the year, the second the month (zero-indexed) and the third the day (one-indexed). In most cases you will want to use the [Moment helper](#momentjs) to format dates. |
|`eggDate`|The day an egg was originally received. See `metDate`.|
|`isEgg`||
|`isNick`||
|`isShiny`||
|`isGhost`|A flag indicating if KeySAVᵉ considers the Pokémon a *ghost*. For more information, read [this](dumping/encrypted-saves.md#ghosts).|
|`isFatefulEncounter`||
|`data`|An array containing the raw pk6 file.|
|`nickname`||
|`notOT`||
|`ot`||
|`version`|The generation the Pokémon was extracted from.|

This is the raw data as saved by the game. This means all of these values are numbers and not numbers, i.e. the IDs used by the game internally. For example, if you had a Charizard, `species` would not contain `Charizard`, but `6`. While this saves space and enables us to easily view the data in different languages, it is highly impractical. For more info on this data, do visit the [Project Pokémon Wiki](https://projectpokemon.org/wiki/Pokemon_X/Y_3DS_Structure).

## Helpers

Introducing *helpers*. In Handlebars a helper is a function taking some input data and computing data to display. They follow a very similar syntax to just showing properties. A helper that doesn't take any arguments looks just like a property: `{{helper}}`. A helper that takes arguments looks like this:

```
{{helper argument1 argument2}}
```

KeySAVᵉ comes with the following helpers that are specific to Pokémon:

|Helper|Arguments|Description|
|------|---------|-----------|
|`box`||The box your Pokémon was dumped from. One-indexed.|
|`row`||The row in your box the Pokémon is in. One-indexed.|
|`column`||The column the Pokémon is in. One-indexed.|
|`level`||The current level of the Pokémon.|
|`hp`||The actual stats the Pokémon has, calculated from IVs, EVs, nature, level and base stats.|
|`atk`|||
|`def`|||
|`spAtk`|||
|`spDef`|||
|`spe`|||
|`speciesName`|||
|`hasAlternateForm`||True if the Pokémon's form is not `0`.|
|`formName`|||
|`natureName`|||
|`abilityName`|||
|`typeName`|`typeId`|Usage example: `{{typeName hpType}}`.|
|`moveName`|`moveId`|Usage example: `{{moveName move1}}`.|
|`itemName`|`itemId`|Usage example: `{{itemName heldItem}}`.|
|`ballName`|||
|`metLocationName`|||
|`eggLocationName`|||
|`ballImage`||Include the ball image on [/r/svexchange](https://reddit.com/r/svexchange).|
|`esv`||The ESV padded to 4 digits.|
|`tsv`||The TSV padded to 4 digits.|
|`tid`||The TID padded to 5 digits.|
|`sid`||The SID padded to 5 digits.|
|`language`|||
|`genderString`|`gender`|Usage example: `{{genderString gender}}`.|
|`gameVersionString`|||
|`stepsToHatch`|||
|`hasHa`|||
|`checkmark`|`condition`|Shows a ✓ if `condition` is true, otherwise show ✗. Usage example: `{{checkmark isShiny}}`.|
|`pentagon`||Show ⬟ if the Pokémon originated from a Generation 6 game.|
|`shinyMark`||Show ★ if the Pokémon is shiny.|
|`markings`||Show ◯△□♡☆◇ or ●▲■♥★◆, each character depending on if the mark is set or not.|
|`regionName`|||
|`countryName`|||
|`ribbons`||An array of Ribbons this Pokémon has. Usage example: `{{#each (ribbons)}}{{this}}{{/each}}`|
|`characteristic`|||
|`esacpe`|`str`|Escape backslashes and quotes.|
|`toJson`|`element`|Stringify the passed parameter to JSON.|
|`eval`|`expression`|Takes any JavaScript expression and evaluates it. If you separate multiple expressions by a semicolon all will be evaluated, but only the value of the last will be used. In this scope, the localization data for the current language is available as `local` and the Pokémon object is available as `pkm`.|

If a helper and property have the same name, the helper takes precedence. This means that `{{box}}` will be one-indexed if you use it.

Furthermore the following helpers are included:

### Moment.js

The moment helper, exposing the entire moment library for formatting dates, it works the following way:

  * `{{moment method=null}}` means `moment().method()`
  * `{{moment date method="parameter"}}` means `moment(date).method("parameter")`

For all the options that are available to you, check out the [moment.js docs](http://momentjs.com/docs/#/displaying/), e.g.

```
{{moment metDate format="YYYY-MM-DD"}}
```

formats the met date as `YYYY-MM-DD`.

### Dashbars

Additionally the [dashbars](https://github.com/Cu3PO42/dashbars) library is available for all your logic needs.

## Block helpers

There are also block helpers that can wrap other templates. Without getting into too much detail, the most important ones are:

### If/Else

```
{{#if condition}}
    STUFF
{{else}}
   THINGS
{{/if}}
```

This shows `STUFF` if `condition` is true, otherwise `THINGS`. The `else` branch is optional.

### Each

```
{{#each array}}
    {{this}}
{{/each}}
```

{% endraw %}

This repeats the template for every element in the array and sets the context to that object.

{% include "footer.md" %}
