# Fallout76-Strings

This is a set of Header Processor rules and Fallout 76 String Dictionaries for use with [xTranslator][xtranslator-nexus].  
Primary language as English, with EN -> EN translations with the purpose of tagging and otherwise bettering the user interface.  
The vision of these translations is to improve the user experience and interface of Fallout 76, as well as allow for more efficient inventory management using mods like Invent-O-Matic [Pipboy][inventomatic-pipboy-nexus] + [Stash][inventomatic-stash-nexus].  
While this is primarily a collaboration between Halvkyrie and MrsBlobby for more personal use, the intent behind making this public is to show some of what can be done using xTranslator, and to provide some form of reference and examples.  
Most of this isn't intended to be plug and play, but you are welcome to make use of and build upon what is in this repository.

---

## DISCLAIMER

Some of these rules and dictionaries are personalized. They may not be suited for your use, and this can cause interference with mods related to interface and inventory that are dependent on item names and similar.  
These translations can streamline many aspects of inventory management, just as well as cause complications. If you use [Invent-O-Matic Pipboy][inventomatic-pipboy-nexus] or [Invent-O-Matic Stash][inventomatic-stash-nexus], please make sure you update your configs accordingly.  
**YOU COULD LOSE YOUR ITEMS!** - Please look at what is being changed before you use any of these string edits in the game.  

---

## Header Processor Rules

A list of the different Header Processor rulesets and a short summary of what they do  

### Dynamic Naming Rules

This aims to strip away all the unnecessary parts of the dynamic naming system for things like weapons and armour, to make naming more unified.  
Due to technical limitations, certain weapons will still have their name affected by things like barrel/grip combos. As an example an Enclave Plasma Gun can end up as Enclave Plasma Pistol, Enclave Plasma Rifle, and Enclave Plasma Gun.  
This all could be changed in the ESM, but that's off limits. Therefore it has been handled this way  


### Shared Tagging Header Rules

This is the more personalized set of tagging rules. These are for appending a tag at the end of item names to streamline Invent-O-Matic usage.  
This covers a lot of items like common, seasonal, nontradeable ++ plans, chems, misc items, thrown weapons junk. Many are categorized so they are easy to filter for dropping.  
These may be good for reference regarding how to set up Header Rules, but you really should consider how much this affects if you are thinking of using these as-is.  

## Dictionaries

A list of the Dictionaries and a brief overlook of what they are for  


### Shared Strings

Much like the Shared Tagging Header Rules, this is the personalized dictionary. Similarly made for tagging item for streamlined Invent-O-Matic use, but with some other tweaks too.  
Certain items, **C**onstructible **OBJ**ects etc have been edited to have more unified naming for better sorting. Some items have rarity as a comment.  
Some tags here end up incomplete if not used with the related header rule set.  

---

## TODO

* Write better usage notes, especially regarding font/icons
* Header Processor Rules
  * Tagging for Plants based on their plant type, like flowers (Both FLOR and ALCH). Relevant mainly for Gamma Green Tea
  * Tagging for Power Armour plans based on "Tier"
  * Icon for **Q**uest and **E**vent **UN**i**Q**ues, and tagging for unique items' WEAP records (not just the current INNR WNAM ones)
  * Icons as prefix for Lunchbox + Scout's banner misc effects


---

# Attribution

The main license for this project itself is the MIT License, available in the LICENSE file.  
This project does however make use some use of resources from other sources. The full licenses for these are available within the Licenses folder.  

## Font Awesome Free
Uses [CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/) for its icons in .svg format  
This project uses several icons from [Font Awesome][fontawesome] Free. A really lovely resource that's very fitting for this type of use.  
Some are unedited, and these have attribution embedded within the .svg files themselves.  
However, some are also edited, such as the cube-star icon. And editing them in Illustrator seems to remove the embedded attribution unfortunately.  

## Roboto Condensed
Uses [SIL OPEN FONT LICENSE Version 1.1](https://openfontlicense.org/open-font-license-official-text/)  
The [Roboto Condensed][robotocondensed] font has been used to create some of the icons where text is used.  



[xtranslator-nexus]: https://www.nexusmods.com/starfield/mods/313
[xtranslator-gh]: https://github.com/MGuffin/xTranslator/
[inventomatic-pipboy-nexus]: https://www.nexusmods.com/fallout76/mods/2324
[inventomatic-stash-nexus]: https://www.nexusmods.com/fallout76/mods/2335
[fontawesome]: https://fontawesome.com/
[robotocondensed]: https://fonts.google.com/specimen/Roboto+Condensed