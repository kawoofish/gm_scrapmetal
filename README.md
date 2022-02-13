# gm_scrapmetal "Final Edition"

## Summary

Repository to host the Valve Map Files and assets used in the Garry's Mod map "Scrap Metal". 

## For mappers interested in using the map files

Check out the Releases to get a zip file of everything needed

## Instructions for mounting assets for use in Hammer(++)

1. In your Source game of choice (I used Half-Life 2 and Source SDK 2013 MP for development), make sure you have a "custom" folder inside your root game directory

2. Generally, the custom folder should be in there already, but if not, you can make one. See the appendix below for more info

3. At some point with the SteamPipe update, Valve enhanced custom asset usage by allowing you to make folders within a "custom" folder, instead of mounting on top of the materials/models

4. Here's an example of what mine looks like: "...\steamapps\common\Source SDK Base 2013 Multiplayer\hl2\custom\gm_scrapmetal_v5"

5. Unzip the "assets_gm_scrapmetal_v5" into the custom folders

6. Re-open Hammer, and you should be good to go!


Couple of notes when "packaging" these assets in releases:

1. I use "PakRat" to package all of the assets for release, however, there are probably more advanced and user friendly tools to do this as well.

2. In PakRat, I use the "Scan" button and then point to my "gm_scrapmetal_v5" folder inside "custom". This picks up almost all of the assets (more on that below)

3. If you are planning on keeping the color correction file (cc_scrapmetal.raw), you may need to "Add" this file on its own.
Add the file in, AND make sure to set the filepath reference to "blank". We don't want to leave the relative file reference in, it should be at the "root" asset level (that's how it's defined in Hammer)

4. For whatever reason, it seems that the 3D skybox building models don't automatically find the required textures when packing. Add those in manually (inside materials/models/props_unique) AND make sure to localize the filepath references


## Disclaimer

Sachs & Hale, Calhoun Brewing Company, and Westlake Laboratories are all fictional logos that I made up. Any resemblance to actual corporations is purely coincidental. Assets included come from Counter-Strike: Source and Half-Life 2: Episode Two, which are both owned by Valve Corporation. I am the sole developer of this map, while I have taken feedback and used it from a lot of others, the VMF (Valve Map File) has only been worked on by me. I used to be very protective of it and would not distribute it out, but over time I've decided to release it for public use as it's better off not being attached only to me. You are free to use the map files in part or in whole for your own development or gamemode specific tuning. Credit to me, "Kawoofish", is appreciated but not required. If you need help with using the map files, I am always willing to try my best and help out
