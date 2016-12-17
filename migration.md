# Migration from KeySAV2

KeySAVᵉ is fully backwards compatible to KeySAV2 keys and format strings.
Note that KeySAV2 originally required you to save your game twice (with a soft reset in-between)
every time you wanted to view the data. I removed that requirement around December 2014
but had to change the breaking process and keys a little bit. KeySAVᵉ is compatible
with both, but if you use files from the old breaking process, the restriction of
having to save twice will apply, too. If at a later point you want to upgrade your key,
follow the instructions [here](dumping/encrypted-saves.md).

To import keys from your KeySAV2 installation, go to the `Breaking` tab and choose to
either let KeySAVᵉ scan your home directory for any KeySAV2 installations (up to
five folders nested) or specify an installation explicitly. Either the folder
containing `KeySAV2.exe` or the `data` folder are fine.

The keys will be saved automatically (or used to improve existing keys) and the
formatting options will be added as instances of the `Legacy (KeySAV2)` plugin
ready for you to be used.
