# FAQ

This section will be expanded as questions are asked:

## Some slots don't show up properly for me. What can I do?

When you initially create keys, KeySAVᵉ doesn't know how to decrypt all slots yet. For more info read [this](dumping/saves.md#ghosts).

## KeySAVᵉ shows Pokémon that aren't actually in the save!

That can sometimes happen when your key is not yet complete and is a direct consequence of how the decryption works. For more info read [this](dumping/saves.md#ghosts).

## TEA is not working for me! Nothing happens when I click `Dump Trade`.

This bug was related to a corrupt configuration file and was fixed in version 1.2.2. Please update :)

## How do I export my Pokémon?

KeySAVᵉ can copy your dumping output to the clipboard, save it to a file or save the `pk6` files. Use the three buttons directly over the dumping output.

## Why is KeySAVᵉ so big?

KeySAVᵉ is based on GitHub's Electron. This means that it includes a full installation of Chrome and Node.js. And then there is the sprites
used for the pretty output that take up about 19MB. The application code itself is barely 3MB big...

## I'm on Mac and it says the app couldn't be opened because it is from an unidentified developer.

This 'error' occurs because I am not a member of Apple's developer program, but it is easily circumvented. Just locate `KeySAVe.app` in the finder, right click and click open. It will now give you the option to open the application anyway. You only have to do this the first time you open KeySAVᵉ.

## I'm on Windows 10 and it says the computer was prevented from harm and doesn't open the app.

Just click on 'more information' and an open button will appear. You only have to do this once.

## I'm on Windows and when trying to extract the zip file, it tells me the file name was too long for the destination.

~~This is a limitation of Windows. Please delete the extracted folder and extract the ZIP again to a folder closer to the root of your hard drive. For example `C:\KeySAVe`.~~ This issue should be fixed since version 1.1.1.

## I can open my files, how do I find my TSV?

In the options tab, select the TSV formatting. Now you can read your TSV off of any Pokémon that you captured or hatched yourself.
