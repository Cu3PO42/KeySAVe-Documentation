# Formatting your Pokémon

So you have found a way to dump your Pokémon, cool! By default KeySAVᵉ will display your Pokémon in its 'pretty' output. It is great for looking what's in your boxes, shows a lot of useful and of course it looks good (duh!). However it is not so great if you want to get a quick overview at all the Pokémon in your boxes or want the data in a copy-pastable format.

As such there are various different output modes. KeySAVᵉ relies on plugins to do its formatting and comes with a few by default, but you can also [write your own](/formatting/api-documentation).  
The following plugins are preinstalled:

  1. The [pretty output](/formatting/pretty.md) that is enabled by default.
  2. A [Handlebars](/formatting/handlebars.md) powered general purpose formatting plugin that can generate arbitrary HTML from your templates.
  3. A [Reddit](/formatting/reddit.md) oriented formatting plugin, that renders tables like they would appear on [/r/svexchange](https://reddit.com/r/svexchange) and generates the necessary Markdown so you can insert them there.
  4. A [legacy](/formatting/legacy.md) plugin, that understands the formatting strings used by KeySAV2 including all additional options added by Kaisonic and renders them exactly as KeySAV2 would.

Every plugin may specify if there are intended to be multiple configurations of it (Handlebars, Legacy) or not (Reddit, Pretty). It may also come with any number of default options. These default options may not be modified by you.  
You can however create new configurations by clicking the plus or clone any formatting option (makes the clone editable) by clicking the pen.

To select any of your formatting options use the `Formatting Options` dropdown menu. Default options are marked with a closed lock. You can change the name of any non default option (that is also not the only instance of a plugin) in the text field to the right of the drop down. Use the trash can to delete formatting options.

You may also change the language that is used to display Pokémon names, etc.

# Advanced topics

Now that you can display all your Pokémon exactly as you want, you may only want to look at some of them, so go ahead and check out [filters](filters.md)!
