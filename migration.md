# Migration from KeySAV2

KeySAVe is fully backwards compatible to KeySAV2 keys and format strings.
Note that KeySAV2 originally required you to save your game twice (with a soft reset inbetween)
every time you wanted to view the data. I removed that requirement around December 2014
but had to change the breaking process and keys a little bit. KeySAVe is compatible
with both, but if you use files from the old breaking process, the restriction of
having to save twice will apply, too. If at a later point you want to upgrade your key,
follow the instructions [here](dumping/saves.md).

Upon first start KeySAVe will scan your home folder up to 5 folders deep for any KeySAV2
installations and import keys and custom format strings. You can also specify a
KeySAV2 installation manually. If at a later time you wish to import other keys or
formatting options, go to the `Breaking` tab and use the importer to select your
KeySAV2 installation. Either the folder containing `KeySAV2.exe` or the `data` folder are fine.

The keys will be saved automatically (or used to improve existing keys) and the
formatting options will be added as instances of the `Legacy (KeySAV2)` plugin
ready for you to be used.
