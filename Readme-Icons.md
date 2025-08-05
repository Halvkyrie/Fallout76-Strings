# Icons
Yes, icons

## General
Heavily subject to change.
This note is just going to be very rough for a while probably. Here to give some surface level info of what is being done and how it's being done.  
For (Pre)viewing icons like in xTranslator, I recommend installing the .ttf font to your system. This lets you select and use the font within the xTranslator Header Processor, as well as using things like [Windows' Character Map](https://en.wikipedia.org/wiki/Character_Map_(Windows)) for viewing and copying the characters within the font.

## Game Files
The relevant game files for this are going to be:
* `SeventySix - Interface_en.ba2` with its `fonts_en.swf` as this is where the english locale fonts are. Or whatever other localization archive you have/want to use
* `SeventySix - Interface.ba2` with its `\interface\fontconfig_en.txt` as this is where the "valid characters" are listed, under `validNameChars` and `validBookChars`.

## Tools

### [Fontello](https://fontello.com/)
For generating the actual font .ttf and whatnot using SVG icons, and associating them with unicode characters. This seems to be pretty much spot on for this kind of use.

### [FontForge](https://fontforge.org/)
For certaion operations Fontello can't handle. So far used this to convert a .ttf font into an .svg font that could be loaded by Fontello.

### [JPEXs Free Flash Decompiler (FFDec)](https://github.com/jindrapetrik/jpexs-decompiler)
This will likely not change. Used for viewing and editing the game's interface files (.swf).  
Necessary for changing/extending the in-game fonts.

### [xTranslator](https://www.nexusmods.com/starfield/mods/313)
The reason this is being done in the first place. xTranslator is here also used to patch the game's Interface.ba2 archive using the Header Processor Wizard.  
This seems to be the easiest way to do it, though using a tool like [BSArch](https://www.nexusmods.com/newvegas/mods/64745) (Which I personally use for most packing of .ba2 archives) or Archive2 should work fine.