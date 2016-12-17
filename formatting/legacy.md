# The Legacy (KeySAV2) formatting plugin

This formatting plugin supports usage of formatting strings from KeySAV2. It is provided for backwards compatibility and to make the migration easier for you. If you are looking to create a new format string or are new to KeySAV in general, I strongly recommend you check out the [Handlebars plugin](handlebars.md) instead. It is a lot more powerful and versatile. This formatting plugin will also not be updated for uses sepcific to Generation 7 games. Regardless, here is a guide:

The header is shown before your dumping output or before every box should you choose to split them. A sensible default can be generated from your format string by clicking the reload button to the right of the text field.

Your format string may contain sequences that match `{\d+}` (this is a regular expression and means an opening curly brace preceded by at least one digit and then a closing curly brace). These sequences will be replaced by Pokémon data in your dumping output. The following values have a defined equivalent:

| Number |Meaning|
|--------|-------|
|`0` |Box|
|`1` |Slot(Row, Column)|
|`2` |Species|
|`3` |Gender|
|`4` |Nature|
|`5` |Ability|
|`6` |HP IV|
|`7` |Attack IV|
|`8` |Defense IV|
|`9` |Sp. Attack IV|
|`10` |Sp. Defense IV|
|`11` |Speed IV|
|`12` |Hidden Power Type|
|`13` |ESV|
|`14` |TSV|
|`15` |Nickname|
|`16` |OT Name|
|`17` |Ball|
|`18` |TID|
|`19` |SID|
|`20` |HP EV|
|`21` |Attack EV|
|`22` |Defense EV|
|`23` |Sp. Attack EV|
|`24` |Sp. Defense EV|
|`25` |Speed EV|
|`26` |Move 1|
|`27` |Move 2|
|`28` |Move 3|
|`29` |Move 4|
|`30` |Egg/Relearn Move 1|
|`31` |Egg/Relearn Move 2|
|`32` |Egg/Relearn Move 3|
|`33` |Egg/Relearn Move 4|
|`34` |Shinyness|
|`35` |Is Egg|
|`36` |Level|
|`37` |Region|
|`38` |Country|
|`39` |Held Item|
|`40` |Language|
|`41` |Game|
|`42` |Slot in Box|
|`43` |PID|
|`44` |Gen. 6 Mark|
|`45` |Dex/Species Number|
|`46` |Form|
|`47` |Is HP IV Perfect|
|`48` |Is Attack IV Perfect|
|`49` |Is Defense IV Perfect|
|`50` |Is Sp. Attack IV Perfect|
|`51` |Is Sp. Defense IV Perfect|
|`52` |Is Speed IV Perfect|
|`53` |Perfect IV Count|
|`54` |IV Sum|
|`55` |EV Sum|
|`56` |Egg Received Date (YYYY-MM-DD)|
|`57` |Met/Hatched Date (YYYY-MM-DD)|
|`58` |Experience|
|`59` |Dump Count Number|
|`60` |Infected with Pokérus|
|`61` |Cured from Pokérus|
|`62` |OT Gender|
|`63` |Met Level|
|`64` |OT Friendship|
|`65` |OT Affection|
|`66` |Minimum Steps to Hatch|

In addition to that, a number of settings are available:

  * Show ESV for hatched Pokémon (or leave it blank)
  * Split Pokémon into boxes (or show them as one big table)
  * Show/hide/mark [ghosts](../dumping/encrypted-saves.md#ghosts)

{% include "footer.md" %}
