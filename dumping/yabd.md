# Dumping your Pokémon using YABD

YABD is a small piece of software that dumps your boxes using an exploit in the 3DS webbrowser ('spider'). For this you need any 'old' 3DS, 3DS XL or 2DS with a firmware version between 9.0.0 and 9.5.0-22. A New 3DS will NOT work.

## Usage

1. Download the YABD [`code.bin`](https://drive.google.com/file/d/0B1vPoiWMLosrWmNkU05rS2xsVHM/view?usp=sharing) and place it at the root of your SD card.
2. Launch the game and load your save.
3. Go to the home menu, but do not exit the game.
4. Open the web browser and go to [http://dukesrg.github.io/?code.bin](http://dukesrg.github.io/?code.bin). It is recommended that you bookmark this page.
5. The browser will exit and you will be returned to the home menu.
6. Exit your game.
7. There is a new file `boxes.bin` at the root of your SD.
8. Open this file in KeySAVᵉ to view your data.

## Troubleshooting

If the browser does not exit or there is no `boxes.bin` on your SD card, please clear your history and cookies in the browser settings and try again. It it still does not work, try to initialize the your browser's save data.

## Credits

Special credits go to SciresM on whose code this is based and Yifanlu for reversing Gateway and creating Spider3DSTools.

## A final note to everyone who still uses this method

At the time of writing this it has been almost been a year since the spider exploits have been patched. If you are still using this, you have access to Homebrew and can downgrade to 9.2.0 and run a CFW which will still allow easy checking, but also allow you to use your 3DS online again. I recommend you follow the first three parts of [Plailect's guide to A9LH](https://github.com/Plailect/Guide/wiki) for this.

{% include "footer.md" %}
