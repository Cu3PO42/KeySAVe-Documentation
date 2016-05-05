# FAQ

This section will be expanded as questions are asked:

## Some slots don't show up properly for me. What can I do?

When you initially create keys, KeySAVe doesn't know how to decrypt all slots yet. For more info read [this](dumping/saves.md#ghosts).

## KeySAVe shows Pokémon that aren't actually in the save!

That can sometimes happen when your key is not yet complete and is a direct consequence of how the decryption works. For more info read [this](dumping/saves.md#ghosts).

## How do I export my Pokémon?

KeySAVe can copy your dumping output to the clipboard, save it to a file or save the `pk6` files. Use the three buttons directly over the dumping output.

## Why is KeySAVe so big?

KeySAVe is based on GitHub's Electron. This means that it includes a full installation of Chrome and Node.js. And then there is the sprites
used for the pretty output that take up about 19MB. The application code itself is barely 3MB big...
