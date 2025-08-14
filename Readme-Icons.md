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

---

# Setup

## Font

### Build
The icon .svg files are in /Icons/Icons/  
Each icon should be mapped to a unicode character code as defined in /Icons/CharacterMap.csv (and no I don't have any automation for this. but I wrote it to have a point of reference)  
As long as you are able to use this to create a .ttf font file, you can use whatever method/software to do this  

Fontello works fine for this purpose. With Fontello, you should be able to simply select all the icon SVGs and drag+drop them into fontello.  
Drag from the *first* SVG in the list (00__name.svg) since whichever file you drag from will be loaded first in fontello. This is just to avoid unnecessary manual work reassigning character codes.  
Fontello assigns icons to character codes starting at E800 so the regular icons will start from there and match the Character Map. Currently the character-in-box icons will have to be manually assigned to E000-E00F.  
After the icons have been imported and correctly assigned to a character code, download the font, and ideally install the .ttf font.  

### Add to Game Fonts
Extract/Obtain `fonts_en.swf` and `\interface\fontconfig_en.txt`. xTranslator loads these from `...\Fallout76\Data\Interface\` so it's convenient to move them there.  
Using FFDec, open the swf. Game fonts are found under Fonts. The 3 `$MAIN` labeled fonts are the main relevant fonts to edit.  
To Edit/Extend a font, select the font then select the `Embed...` option in the bottom right. This brings up a font embed menu, from where you can select a font and enter/select which characters to embed.  
Select the relevant font installed on your system, or a .ttf file. /Icons/CharacterList.txt lists all the relevant characters, so copy + paste these into the `Individual Characters` box in FFDec, and select OK to embed.  
Repeat this process for each relevant font  
In FFDec under Scripts you can find definitions of unicode character ranges for each font. FFDec however does update this when you embed new characters in a font.  
Once this is done, that's all that's required on the FFDec side, so you can save and close.  
Open fontconfig_en.txt in your text editor of choice. This file is what maps out the game fonts, and what characters are considered valid.  
To extend the valid characters, simply add the relevant characters to `validNameChars` and `validBookChars`. So copy the character list and paste them at the end, within the "".  
With these files edited, all that's left is patching the game's interface .ba2 archives with the new files.  
xTranslator does this easily via the top menu bar \[Wizards\] -> \[HeaderProcessor Wizard\], using the `Patch Game Files` button. Making a backup first is advisable.  

### Make use of
All that's left at this stage, is making use of the new characters in the game strings.  
The Character Map program can be used to view/copy characters within a font. This allows for easier use of them in xTranslator.  
The Header Processor can also be set to use your new font, which makes previewing and working easier.  