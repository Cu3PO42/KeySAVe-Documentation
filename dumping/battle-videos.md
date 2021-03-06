# Using Battle Videos to dump your data

Using Battle Videos you can check up to 6 Pokémon at the same time of which at least one needs to be battle ready (that means you won't be able to check 6 eggs at the same time). You also need to find someone who will battle you every time you want to check any Pokémon (or use a second console). As such this method is very inconvenient. The only situation when this method is recommended it to check a Pokémon that you may or may not soft-reset.

## Requirements

* The VS Recorder. You obtain it in Kiloude city after beating the Elite 4 in XY and at the Battle Resort in ORAS. In Sun and Moon you receive it as soon as you reach the first PokéCenter.
* A friend that is willing to battle you.
* Go to the games options and disable forced saving.

## Set Up

You can store up to 100 battle videos per game on your SD card. Each of them is stored in a *slot*. You have to break the encryption for each slot separately and you can only decrypt slots that you have a key for. However creating that key is a one time process (per slot). The game will always use the lowest available slot, so make sure to only use the slots you have broken.

A key will always be able to decrypt your own party, but it may or may not be able to decrypt your opponent's Pokémon at the same time. This depends on whether your opponent has followed the following steps as well during the creation of the key.

During the following steps you will be asked to access your battle videos, they're stored in one of the following folders on your SD card, where an asterisk means 'any folder':

Game|Folder  
--|--
X/Y|`/Nintendo 3DS/*/*/extdata/00000000/0000055d/00000000`  
OR/AS|`/Nintendo 3DS/*/*/extdata/00000000/000011c5/00000000`
S/M|`/Nintendo 3DS/*/*/extdata/00000000/00001648/0000000`
US/UM|`/Nintendo 3DS/*/*/extdata/00000000/00001b50/00000000`

The file sizes for Battle Videos are 28,256 bytes for Generation 6 games and 27,584 bytes for Generation 7 games.

1. Make sure you have at least two Pokémon in your party.
2. Start a battle, enter exactly one Pokémon and forfeit.
3. When asked to save the battle video, say yes.
4. Close your 3DS, take out the SD card and put it into your computer.
5. Go to the appropriate folder for your game.
6. Copy the most recently modified file with the correct size to a folder of your choice and append `-1` to the name. **Never** save any data to the KeySAVᵉ folder itself.
7. Now put your SD into your 3DS again.
8. Delete the Battle Video you just created in the game.
9. Start a battle and enter any Pokémon first and the one you used in step 2 second and forfeit.
10. When asked to save the battle video, say yes.
11. Close your 3DS, take out the SD card and put it into your computer.
12. Go to the appropriate folder for your game.
13. Copy the file to a folder of your choice and append `-2` to the name.
14. Now start KeySAVᵉ and go to the Breaking tab.
15. Click on *File 1* and open the video from step 6.
16. Click on *File 2* and open the video from step 12.
17. You should now see a dialog that a key has been created, it will be saved automatically. If you get an error, you have not followed the instructions correctly, please start over.

Now that the boring part is over, let's get right to dumping your Pokémon.

## Dumping your Pokémon

If you are using a Generation 6 game, disable forced saving in the options.

1. Hatch any eggs that you want to check.
2. Put the Pokémon that you want to check in your party.
3. Make sure that the next free battle video slot is one that you have previously done the breaking procedure for.
4. Start a battle and forfeit. If you are using a Generation 7 game, do not use an online battle since the game will save and your eggs will stay hatched! You have to use a local battle or a Battle Royal. Unfortunately you can only enter three Pokémon in a Battle Royale and can't enter two of the same species.
5. When asked to save the battle video, say yes.
6. Reset your game.
7. Close your 3DS, take out the SD card and put it into your computer.
8. Go to the dumping tab in KeySAVᵉ, click open file and select the battle video.

You're all good to go now!

{% include "footer.md" %}
