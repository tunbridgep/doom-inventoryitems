# Simple Inventory Items #

## About ##

This mod dynamically converts a large number of powerups into usable inventory items in a mod-friendly and compatible way. Future versions are also planning to remove the inventory tag on Hexen puzzle items, so they don't clog up the inventory screen.

## Feature Overview ##

This mod has the following features, all of which are designed to be optional and fully customisable:

- The ability to dynamically convert Soulspheres, Megaspheres, and other powerups into items usable from the inventory screen.
    - This is done in a compatible way, so powerups that are replaced by versions from other mods (eg Brutal Doom) will be handled correctly
- A configurable "health minimum", that will automatically use any healing item (eg Soulsphere) immediately upon pickup if the players health is low enough
- A dedicated button to use the last-acquired inventory item.
- A dedicated button to use the best healing item available. This is the item that will restore the most health and armor with the least excess health wastage.

## Why Does This Exist? Doom is an Action Game! Making it more like Heretic destroys the Balance! ##

Maybe. This mod is configurable for a reason. Still, I am open to balance suggestions and changes.

This started as an exploration of zscript and it's features, especially with dynamically modifying actors through script, such as applying the bFloatbob flag. I found it added an extra level of depth to gameplay, especially when combined with other mods that further restrict the player and make using items at the right time a necessity, such as [my Simple Saving mod](https://github.com/tunbridgep/doom-simplesaving).

## Installation ##

Please note that the repository only contains source code with no transient data (no zscript include files or compiled ACS script)
**Premade release versions are ready to go on the [Releases page](https://github.com/tunbridgep/doom-inventoryitems/releases).**

If you wish to build it yourself you can do so using the following steps:

1. Clone or download the repository
2. Create an include file for all files in the zsc directory. Zscript includes are discussed in detail [here](https://zdoom.org/wiki/ZScript)
3. [Zip the contents of the src directory as a pk3](https://zdoom.org/wiki/Using_ZIPs_as_WAD_replacement), then run in GZDoom using the -file parameter or using another method.

Alternatively, for a much quicker build experience, a config file is included for use with my [doom_quickbuild](https://github.com/tunbridgep/doom_quickbuild) utility.

## Planned Features ##

- Support for other iwads, such as Heretic/Hexen/Strife. Mainly to support the opposite - make items not go into the inventory and instead get used immediately
- Removing Hexen puzzle items from the inventory

## Contributing ##

There are many ways to contribute to the project. The easiest way is by filing a bug report or feature request, however code and documentation contributions are welcome. Documentation of the various features and lighting modes is especially important. All pull requests are welcome, however code should generally follow these rules:

1. ZScript should always be preferred over DECORATE and ACS. This mod currently uses no ACS.
2. Features should be as compatible as possible. Changing or overriding a function or flag on an actor is preferred over simply making a new actor.
3. Almost no thought has been put into multiplayer. This mod has not been tested at all with multiplayer. It is not required for contributions to consider multiplayer, however some consideration would be appreciated. A good example of small considerations is considering whether a console command should exist within the user or server space, and using netevents wherever possible.
4. Consideration should be made for hubs. There is not a significant number of popular hub maps for Doom, however this mod is intended to eventually support Hexen, at which point hub map support will be required. This is usually as simple as checking for e.Reopen when defining/using an event handler.
5. Documentation should be clear. Pull requests and commits should be well documented. Code should be documented where necessary if the intention or logic is not clear. Please follow the existing code style.

For questions or feature suggestions, feel free to create an issue on the issues page, or email me at tunbridge.p+doom@gmail.com

## Credits ##

* Some inventory images used for PB items are edited version of PB sprites. Get PB [here](https://github.com/pa1nki113r/Project_Brutality)

## Other Stuff ##

Checkout my other mods on github

* [Simple Teleporter Effects](https://github.com/tunbridgep/doom-simpleteleportereffects) - add particle effects to any teleporter in any map in a compatible way
* [Simple Saving](https://github.com/tunbridgep/doom-simplesaving) - remove save scumming and tie saving to resource usage.
* [Simple Inventory Items](https://github.com/tunbridgep/doom-inventoryitems) - make most Doom powerups usable from the inventory bar in a compatible way.
* [Simple Completion Rewards](https://github.com/tunbridgep/doom-simplecompletionrewards) - be rewarded for getting 100% completion in a map. Highly configurable.
* [Flashlight Mod](https://github.com/tunbridgep/doom-flashlight) - adds a usable flashlight, the ability to darken the map, a dynamic system for enemy and player stealth, and more.
