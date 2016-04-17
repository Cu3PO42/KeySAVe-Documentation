# Using Battle Videos to dump your data

Using Battle Videos you can check up to 6 Pokémon at the same time of which at least one needs to be battle ready (that means you won't be able to check 6 eggs at the same time). You also need to find someone who will battle you every time you want to check any Pokémon. As such this method is very inconvenient. The only situation when this method is recommended it to check a Pokémon that you may or may not soft-reset.

## Requirements

* The VS Recorder. You obtain it in Kiloude city after beating the Elite 4 in XY and at the Battle Resort in ORAS.
* A friend that is willing to battle you.
* Go to the games options and disable forced saving.

## Set Up

You can store up to 100 battle videos per game on your SD card. Each of them is stored in a *slot*. You have to break the encryption for each slot separately and you can only decrypt slots that you have a key for. The game will always use the lowest available slot, so make sure to only use the slots you have broken.

A key will always be able to decrypt your own party, but it may or may not be able to decrypt your opponent's Pokémon at the same time. This depends on whether your opponent has followed the following steps as well during the creation of the key.

During the following steps you will be asked to access your battle vidoes, they're stored in one of the following folders on your SD card, where an asterisk means 'any folder':

Game|Folder  
--|--
X|`/Nintendo 3DS/*/*/extdata/00000000/0000055d/00000000`  
Y|`/Nintendo 3DS/*/*/extdata/00000000/0000055e/00000000`
OR|`/Nintendo 3DS/*/*/extdata/00000000/0011c400/00000000`
AS|`/Nintendo 3DS/*/*/extdata/00000000/0011c500/00000000`

1. Make sure you have at least two Pokémon in your party.
2. Start a battle, enter exactly one Pokémon and forfeit.
3. When asked to save the battle video, say yes.
4. Close your 3DS, take out the SD card and put it into your computer.
5. Go to the appropriate folder for your game.
6. Copy the file to a folder of your choice and append `-1` to the name.
7. Now put your SD into your 3DS again.
8. Start a battle enter any Pokémon first and the one you used in step 3 second and forfeit.
9. When asked to save the battle video, say yes.
10. Close your 3DS, take out the SD card and put it into your computer.
11. Go to the appropriate folder for your game.
12. Copy the file to a folder of your choice and append `-2` to the name.
13. Now start KeySAVe and go to the Breaking tab.
14. Click on *File 1* and open the video from step 6.
15. Click on *File 2* and open the video from step 12.
16. You should now see a dialog that a key has been created, it will be saved automatically. If you get an error, you have not followed the instructions correctly, please start over.

Now that the boring part is over, let's get right to dumping your Pokémon.

## Dumping your Pokémon

1. Put the Pokémon that you want to check in your party.
3. Start a battle and forfeit.
4. When asked to save the battle video, say yes.
5. Close your 3DS, take out the SD card and put it into your computer.
6. Go to the dumping tab in KeySAVe, click open file.
7. Go to TODO and select the battle video you want to view.

You're all good to go now!

## Advanced topics

Want to display your Pokémon differently? Check out the [Formatting Options](../formatting.md).  
Want to filter the Pokémon to be displayed (well, there really aren't too many with battle videos, so you may not want this)? Check out the [filters](../filters.md)!  
