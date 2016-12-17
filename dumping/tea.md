# Dumping Pokémon shown to you in a trade using TEA

Traditionally if someone wanted to get their eggs or Pokémon checked and couldn't use any of the methods themselves, the Pokémon had to be traded to someone with access to any of the checking methods and then traded back. Overall that takes about a minute per Pokémon. The TEA (**T**rading is an **E**xcessive **A**ssignment) method only requires someone to *show* you the Pokémon and it will read it straight from the 3DS memory.

## A Warning to Users

If you get your Pokémon checked with TEA, please make sure to only show your partner the Pokémon you actually want to get checked and no others. A malicious users could clone your valuable Pokémon otherwise. This applies especially to Generation 7 since all Pokémon you move your cursor over are shown.

## Setup

* Make sure you have KeySAVᵉ 1.2.0 (1.4.0 for Generation 7 games) or later. If you currently have version 1.1.1 or later, you will receive an update, otherwise please [download a new version](https://github.com/Cu3PO42/KeySAVe/releases).
* Install NTR CFW on your 3DS. This requires that you currently run a CFW such as Luma3DS. If your 3DS is on version 11.0 or later, you will need a hardmod to obtain this, otherwise you can follow the first three parts of [this guide](https://github.com/Plailect/Guide/wiki). Once you have a CFW, install [this](https://github.com/astronautlevel2/BootNTR/releases/latest) CIA file and copy the `ntr.bin` from [here](https://github.com/44670/BootNTR/files/222950/NTR_3.4PREVIEW2_STARTER_KIT.zip) if you are on a N3DS, or from [here](https://github.com/44670/BootNTR/releases/download/3.2/NTR.3.2.zip) if you are on an O3DS to the root of your SD card.
* Find out your 3DS' IP address in your local network. You can either check in your router's configuration interface (I am unable to provide assistance for this) or start one of the many FTP clients for 3DS. Your IP will be on the top screen.

## Dumping Pokémon

1. Open BootNTR on your 3DS' homescreen and wait for it to finish.
2. Open the Pokémon game of your choice.
3. Connect to the internet in game.
4. Press `X`+`Y`, select *Enable Debugger* and press `A` to continue.
5. In KeySAVᵉ, press the TEA button (it looks like a to-go cup) below the text field that shows the currently opened file.
6. Input your 3DS' IP address and click on *Connect*.
7. Enter a trade.
8. As soon as the trade window itself is shown, click *Trade Dump*.
9. Have your opponent show you each Pokémon they want dumped. Every Pokémon should be shown for around a second to compensate for potential connection issues. Generation 7 automatically shows every Pokémon that you move your cursor over, pressing *Show* is not required.
10. Copy the dumped data in the format of your choice.

## Additional functionality

You can also dump your boxes and battle box from the KeySAVᵉ menu!

## Credits

Credits go to [cell9](https://github.com/44670) for creating NTR and therefore making this possible in its current form. Special thanks also go to [/u/Fadx](https://reddit.com/u/Fadx) for providing me with data that the Pokémon shown to you in a trade is relative to and the relative offset itself in Generation 6 games.

## History

A similar method has been available in the past under the name of Instacheck that worked by capturing your 3DS' network traffic. It has been patched shortly after a tool was released to the public.

{% include "footer.md" %}
