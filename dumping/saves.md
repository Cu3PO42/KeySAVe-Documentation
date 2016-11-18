# Accessing your save data directly

KeySAVᵉ can read and decrypt your save data directly. This requires either a digital copy of the game or a Powersaves 3DS if you use a physical copy. If you have a 3DS with access to Homebrew or a Cybersaves device, please read the respective guides instead.

Using this method you can view all 930 Pokémon in your boxes. Viewing your party and battle box is not currently supported. This is one of the fastest ways to check a large number of Pokémon after the initial decryption process is completed.

## Initial decryption

To create the keys needed for the decryption, KeySAVᵉ needs two saves in specific configurations. Please follow the guide exactly as the process will otherwise fail.

This process differs only slightly from the decryption process used by the original builds of KeySAV2. KeySAVᵉ is backwards compatible to that process, so you can use those saves if you still have them, however if you do that, you will be required to save twice to view data in your saves. This process is identical to the one used by my builds of KeySAV2, so if you had one of those, you don't need to do this again.

You will be required to create backups of your save in this process. If you are using

* Powersaves and a physical copy, insert the game cartridge into the device, start the software , click on the `BACKUP` button and name the backup. The file will be located in `C:\Users\<YourUsernameHere>\Powersaves3DS` if you use Windows or `~/Documents/Powersaves3DS` if you use a Mac.
* a digital copy, the saves are stored on the SD card of your 3DS in a folder specific to the game. If you are using X, the path is `title/00040000/00055d00`. For Y, it is `title/00040000/00055e00`. For OR, it is `title/00040000/0011C400`. For AS, it is `title/00040000/0011C500`. For Sun it is `title/00040000/00164800`, for Moon it is `title/00040000/00175e00`. Copy the file there to a folder of your choice on your PC and rename it as you wish. Never save any data to the KeySAVᵉ folder itself.

1. Locate six Pokémon that you caught or breed yourself. They have to originate from the save that you are trying to create a key for. If you can't find enough, catch new ones.
2. Put them into the first row of the first box in your computer.
3. Save your game.
4. Soft reset. (`L+R+Select`)
5. Save your game again.
6. Exit the game.
7. Create a backup of your save as explained above. Name it `16`.
8. Move the six Pokémon from box one to box two. It is important that you preserve their order exactly.
9. Create another backup (DO NOT SAVE TWICE). Name it `165`.
10. In KeySAVᵉ, go to the breaking tab and open `16` as file 1 and `165` as file 2. Click on 'Break'.
11. You should see a success message, your key will now be saved.

**NOTE**: It is possible, but very unlikely (~0.02%), that even if you followed the steps exactly, decryption will fail. In that case, please choose six different Pokémon (replace all of them) and start over.

<a id="ghosts"></a>
### Breaking the encryption for more boxes

**IMPORTANT, DO NOT SKIP THIS SECTION**: After the initial decryption, KeySAVᵉ does not know how to decrypt most of your slots yet. It can only decrypt slots 1-6 in boxes one and two and has the neccessary data to create keys for other slots over time.

To be able to decrypt a slot at all, you need to have opened a save that has that slot empty. To determine which is the empty state you also need to open saves that have two different Pokémon in that slot. Until that happened a slot is not fully unlocked and you may encounter *ghost* Pokémon. That is, either Pokémon that are actually in the save don't show up at all, or Pokémon that are not in the save do show up. KeySAVᵉ knows when a Pokémon might be a *ghost* and most formatting options will either offer you to hide them entirely or mark them as such.

KeySAVᵉ will improve your keys as it sees more data automatically. If you have a lot of backups, KeySAVᵉ can scan them automatically. To do that, go to the `Breaking` tab and click on `Scan Folder` and select the folder containing your saves.

The fastest way to unlock all slots is the following, assuming you have a key that does not require saving twice:

* Empty all boxes.
* Create a backup and open it in KeySAVᵉ.
* Fill all boxes with Pokémon, then save in-game.
* Soft reset. (`L+R+Select`)
* Move around the boxes, i.e. either shift Box 1 to 2, 2 to 3, ... 30 to 31 and 31 to 1, or switch them in pairs, i.e. 1 with 2, 3 with 4, ...
* Save again.
* Create another backup and open it in the Dumping tab in KeySAVᵉ.
* ???
* Profit.

## Accessing your data

To check any Pokémon in your boxes save your game (once is enough) and export the save as described above. Then open the file in KeySAVᵉ's `Dumping` tab. All Pokémon that can be decrypted will be displayed.

{% include "footer.md" %}
