# Filters

The filters may be enabled by clicking the `Enable Filters` button in the dumping tab.

The various options should be mostly self-explanatory, however here are some remarks:

* A perfect IV is normally considered to be 31.
* If you tick the 'Special Attacker' checkbox, the Attack IV will be considered to be perfect when it is 0.
* If you tick the 'Trickroom' checkbox, the Speed IV will be considered to be perfect when it is 0.
* If you select at least one Hidden Power, the IVs 30 and 1 respectively will also considered to be perfect.
* By default the 'Is Shiny' filter will show only hatched shinies. If you want to show eggs, you can
  * tick the 'My SV' chechbox. That will display eggs that will hatch shiny on your current game.
  * input any number of SVs in the textbox below - the egg will be shown if it matches any of those SVs
* Eggs will only be filtered for SVs if the 'Is Shiny' filter is activated as well
* The shiny override will show a shiny if it matches your shiny criteria even if it doesn't fullfill any of the other filters!
* The custom filter is any valid JavaScript expression, if it evaluates to a *truthy* value, the Pokémon will be shown, it will be hidden if it is *falsy*. The Pokémon to filter is available as `pkm` in the context.
