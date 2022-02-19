# gm_scrapmetal_v5 (final edition)

Welcome to the site / repository where I'm hosting the map files and assets used in gm_scrapmetal. There's a couple links and files scattered around so I'll sum up what's going on here:

- [Click to Download Scrap Metal Valve Map Files (VMFs) and assets](https://github.com/kawoofish/gm_scrapmetal/releases/tag/Version-5-Release)

- [Click to view Documentation of known issues and other info on the map files here](/docs.md)

A quick summary: "Final Edition" just denotes that this will be the last major update and rework of the map. I'm happy to work with others and continue support if there are known issues or hotfixes needed, but from my personal experience, I'm satisfied with how this version of the map has turned out, and would like to move on to new maps and ideas. I'm hosting everything here in hopes it will be easy to download the map files and assets, and to share more information beyond just the Steam Workshop page.

# Rambling Retrospective and After Thoughts

I wanted to throw a little recap of some of my level design experience and personal learnings in here. I've talked and worked with a lot of people about level design in Source and it's always an intriguing topic for me. I'll keep this mainly on Scrap Metal's development, and maybe keep a bigger conversation going on another page later

## Getting started

To give a brief history of how I started with all this, I'll jump back to around 2010 or so. I frequented a Garry's Mod Zombie Survival server that had a large map rotation. I did enjoy a lot of the maps and they really did nail the feel of a zombie apocalypse (it helps with the theme of Half-Life 2 based assets and overall grunge feel). However, I felt there was a lack in variety, as you generally would find yourself barricaded in a big house, or some area taken from Half-Life and then reworked a little for gameplay balance. I decided around this time that I wanted to learn how to make my own maps to contribute and to have fun with.

![Zombie Survival](/img/sunrust.jpg)

## Inspiration

By around 2011 or so, I had gotten around with the basics of Source and Hammer (thanks to 3kliksphilip for his YouTube tutorials, very helpful as a beginner). Before Steam Workshop existed or was supported for Garry's Mod, there was a GMod built-in utility called "Toybox" that basically functioned in a similar way. There was also garrysmod.org which hosted a lot of addons in a more manual way as well. I released my first map on there (it wasn't very good but it got the basics out there), and after that I got more comfortable doing edits of existing maps to start.

![first map: long run beta](/img/long_run.jpg)

Eventually, I did get around to creating a zombie survival map, zs_factory_v3, which was originally created by my dear friend Maria. I had the chance to expand it out a bit and improve some of the gameplay loop. It was generally well received (from what I could tell at least), and I had some more confidence to try and make something from the ground up.

![zs_factory_v3](/img/factory.jpg)

At around this time in 2011-2013, there were probably 2 main games I was playing. Garry's Mod, and Battlefield 3 (and maybe some Halo Reach thrown in there). Looking back, Battlefield 3 seemed way ahead in time in terms of graphics, sound design, and the overall gameplay feel. I was just a kid back then with an Xbox 360, and we would always hop on after school to get some more rounds in. While today I would say some of the "cinematic" effects (blue color correction, lens flares, etc.) are a bit overboard, it did help the game keep a unique feel that has aged really well (don't even get me started on Battlefield 2042). I thought, as something to kind of flip the script, what if I made a map that sorta captured some of that feel in GMod?

![Battlefield 3: Close Quarters](/img/bf3.jpg)

## Close Quarters

If you're familiar with Battlefield 3's DLCs, you may remember "Close Quarters", with a more infantry focused setting. While I mainly remember that DLC for Ziba Tower and Donya Fortress, there was another map I enjoyed called "Scrapmetal". And yes, this is where *some* of the inspiration for this GMod map came from, name included. In Battlefield 3, this map was set in a collection of warehouses and foundries in the middle of somewhere, with you the player shooting the place up, which had a lot of destructible elements and bridges to cross.

![Battlefield 3: Scrapmetal](/img/bf3_scrapmetal.png)

While you could remake that map straight from Battlefield 3 (and there is a wonderful TTT version that [Nahte](https://steamcommunity.com/id/Nahte99) made [here](https://steamcommunity.com/sharedfiles/filedetails/?id=228105814&searchtext=scrapmetal)), I wanted to find some way to adapt it to GMod Zombie Survival, and make a somewhat more open map (this goes against a lot of the zombie survival gameplay loop, I later found out). So, with all this in mind, I opened up Hammer and started trying to make something out of it

## Greybox... or not

One thing every level designer should start with is a basic plan on what the map's theme will be, gameplay elements, etc. I have to be honest, looking back as a software developer now to how I started out, I really was never a guy to plan things out or do any documentation. Yep, I just wanted to jump into the code or level design and start breaking stuff, and to some degree this worked out. But sooner or later, I discovered I would hit a wall and be stuck and not know what to do, or how to connect these two pieces together.

![robert yang design](/img/robertyangdesign.jpg)

Greyboxing, or block outs, help define structure and a sense of direction on how you progress on the level. From what I've seen at least, all of the pros do this, and I highly encourage those who are starting out to allocate however much time is needed, to try and plan out the majority of the layout before diving into the fun stuff. This same kind of idea happens in software development, with scrum teams, architecture discussions, and agile planning. As you start detailing and working through, you'll quickly find that maybe you didn't like the area you had planned out, and you'll be able to adapt quicker and make changes on the fly if the layout design is guiding you along the way.

![Valorant blockout](/img/valorant.jpg)

I'm not sure if anyone could tell, but when I started Scrap Metal's development, there was no plan, and no greyboxing or layout done ahead of time. You guessed it, I winged it and created and detailed each area individually. Then I somehow had to connect everything together, and make this map somewhat balanced for zombie survival (it did not turn out that way). This process, while immediately rewarding to see one area you worked on look pretty and detailed, led to a roadblocks and delays along the way. There was a lot of difficulty in figuring out how to where to progress next, and how to fit everything in, and if I had maybe planned the layout better, it could have been a little more cohesive.

![Overview](/img/overview.jpg)

## Spawning in

I'm now gonna talk about each building in Scrap Metal and the inspirations I may have had at the time. This is mainly for me to review my thought process and see where improvements can be made in the future. We'll start with the "Spawn room", a.k.a the big warehouse the player usually starts in (humans in Zombie Survival). Up until the final version, only the top floor of this warehouse was accessible, and the idea was to have a somewhat big, open warehouse as the player start to give a sense of what the rest of the map would feel like

![Warehouse reference](/img/warehouse_ref.jpg)

I do remember distinctly for this spawn room, I referenced some real world pictures of abandoned warehouse, to try and capture that same, eerie feeling of being alone in one. Big windows give a view to outside and are the main light source. There's a water puddle on the ground to give some interesting reflection (I didn't bother adding a prop or source as to why water is there in the first place, immersion ruined!), and a couple of destroyed pieces of concrete. One set piece (and I got the idea from some HL2 mod I can't seem to find now) was the destroyed Combine helicopter through the roof. One thematic element I wanted to have was some clear connections and ideas that this was in the Half-Life 2 setting, and that the area would be a little battle-torn and run down looking

![Helicopter](/img/helicopter.jpg)

In terms of zombie survival gameplay, this room doesn't really do anything except give humans a safe place to spawn (I remember on my old computer spawning into a zombie survival map would usually take me into the middle of the game). There is one room that is potentially usable, although it only has 1 doorway and some holes in the roof. The elevator shafts in the back also did not open until wave 2, to give humans a chance to safely spawn in through wave 1.

![Spawn](/img/spawn.jpg)

In V4, I wanted to better utilize some of this space, or more accurately, the whole building. So I added a big open warehouse underneath, that is mainly empty to give players a build area in Sandbox. I also had what I dub the "Steam room", which is the room on the roof connected to the elevator shafts, and contains some generators, pipes, and machinery. I also had the idea of having this as a HL2 resistance hideout, and have these little lambda marked areas scattered around

![Steam room](/img/roofroom.jpg)

## Atlantic building

This area mainly involved a top floor which had some inspiration from Kleiner's lab, and I wanted to add a little bit of Combine influence. "Office" areas I guess do take up a good portion of the map, and this one started out as a more industrial one in V2, to transition to a more standard office settings in V4. The second floor was actually a very late rework to V4/V5, which I had some inspiration from one of the Battlefield 3 campaign missions, involving the player in an office setting in Paris

![Battlefield 3: Hit and Run](/img/bf3_hit_and_run.jpg)

Not sure what inspired the parking garage, and what made me put it inside the building, but overall, this building provides some large areas, none of which really suited zombie survival barricading areas. The general shape of the building took place first, and I then needed to fill it with rooms and details on the inside. Again, I feel like the layout of this building would have definitely benefited had I blocked it out prior

![atlantic](/img/atlantic.jpg)

## XCCR building

The main setup for this started as some big warehouse which would utilize the "warehouse shelves" which I think came from Counter-Strike. The setup for some shipping operation or something. Since I wasn't very experienced with elevators at the time, staircases became the main way to get up. I originally had the stairwells split between the two sides, but I figured it would make more sense and allow more expansion if I just wrapped the building around the stairwells to give a more cohesive look.

![XCCR Warehouse](/img/xccr.jpg)

The office floor contains a meeting room and some open work areas. I wanted to keep the general feel from V2 to V4 with the slightly claustrophobic office vibe, but one thing I did want to change was the exterior windows not actually leading to a window on the interior. The main reason I probably didn't do this before was the potential visibility optimization nightmare that would come from opening up a bunch of windows vs. a solid wall. With some new Areaportal Window tricks, I was able to manage this by having the windows fade to the correct opaque window texture at a fixed distance. I think the visual effect and aesthetic of having the windows actually function was worth it

![Office](/img/office.jpg)

The top floor is some kind of chemical containment room or something. I didn't really know what to do with it, and there aren't really any rooms or sealed off areas. There is a connecting portion to the office below. This room really goes in on effects with the lens flares sprites, Combine machinery, and the ambient music playing

![Containment](/img/containment.jpg)

## Train depot / lab building

I designed and detailed the buildings in this order above, so I ended up needing something to go in the middle of this circle of buildings. Since HL2 and CS:S have a lot of handy train models, I figured a trainyard would fill some of the space and make sense for the industrial / freight settings. A train "control room" was also on the side, and was expanded in V4. The train depot served as a way to close the gap and connect the buildings, and also having a natural stopping point for the skybox.

![Trainyard](/img/trainyard.jpg)

In V2, this mainly consisted of some electrical rooms and storage rooms. I actually was going to completely scrap this area at first, as I didn't think it really served any purpose on the inside, but I decided to give it a makeover for V4/V5.

![Stairs](/img/stairs.jpg)

The lab that takes up the main area serves as some kind of human / alien experimentation area, with some headcrab containers crashing in. I had some inpsiration from RE2's Umbrella Labs and Escape from Tarkov's Terra Labs designs.

![Lab](/img/lab.jpg)

## Outdoor areas

In Version 2, we had a 3D skybox (inacessible to players) park, and a smokestack. With V4, I wanted to bring this into the playable area, to give a bit of contrast and something different from all the industrial grunge (how realistic a park near an industrial center is questionable).
I also threw in some Half-Life 2 playground elements (ripped straight from the SDK VMFs) for fun physics with the seesaw, carousel, and tic tac toe game.

![Park](/img/park.jpg)

For the longest time, I didn't know what to do with the big concrete space with the smokestack. Then, suddenly, an idea popped into my head one day. From a bird's eye view, the layout for the famous Call of Duty shipment could maybe fit in that space? It turns out, a simple layout with some cargo containers from CoD to Half-Life 2's cargo containers, ended up fitting in perfectly with the setting and the space available. Having a small little outdoor "deathmatch" arena with the "Shipment" layout from CoD ended up working nicely, and also a small chance to add some little pieces and hints of a Half-Life / Combine theme

![Shipment](/img/shipment.jpg)

## Final edition wrap-up

One idea I had floating around was having a night version of the map. A lot of Zombie Survival maps tend to be set at night time, since it fits the setting well and makes things more eerie, but I liked the day version and what it let me do with abandoned, dusty areas (hence the volumetric light models, fog, dustmote effects, etc.) The night version ended up being a fun thing to create and was actually a little more involved than I first thought. Much of the exterior soundscapes needed to be changed (I didn't want active city noise at night time). Lights and some areas had to be tweaked, and the trainyard and park had their lamps turned on. I still wanted to give it a dark feel in some areas, to encourage those who like to use night vision mods or something along those lines.

![Hammer](/img/hammer.png)

Overall, I'm really happy with how this final version turned out. I've already seen there were a few minor mistakes or bugs, but this has been a few months coming, and I'm glad to take this to completion. I'm sure I'll look back on this in the future and think it doesn't hold up, but that's just part of the learning process.

![Hammer2](/img/hammer2.png)

## Closing thoughts and future plans

To be completely honest, I really didn't think this map would get that popular, especially considering my limited Hammer / level design experience going into it. I was kinda surprised how much of an outcry there was when I delisted it, and even today, I'm not quite sure what keeps people coming to the map back all these years later. But it's been a really fun and introspective journey to the past, and it was great to dive back in with a fresh viewpoint. I'll admit, looking back, I did have a bit of an ego when this came and got initially popular, it was a feeling I probably hadn't experienced when I was around 14 or 15 years old, but there are some incredible mods, maps, and addons out there that have shown there's limitless potential in the community

I've definitely sunk a lot of time into Source level design as a hobby, and I'm fortunate that it's been a rewarding one for the most part. I've met a lot of people online and I'm always up to chat about various things relating to level design, Source, and GMod in general. I'll make a brief tangent and say that this map did catapult me into my involvment with "Hunt Down the Freeman", and despite the outcome of that, I am glad I did give a shot and try my best at it. I'll have to make another write up on that experience, as there's a lot to talk about

If you made it this far through a lot of my nonsensical ramblings on what was going on in my head whlie making this map, thanks for your interest and for reading through all this. Level design has been a fun hobby and way of learning for me over this past decade. My full-time job involves a lot of programming, and maybe one day I'll be able to learn about this old Source engine to make a mod or go beyond level design, but maybe that's best saved for another engine or Source 2. For the time being, as long as I've got the ideas churning in my head, I'll try and keep making maps that are fun for me and hopefully for others.

## Resources used and Special Thanks

First up, I'll just start listing out a bunch of people that have provided helpful feedback, praise, bugs and issues needing to be addressed, and everyone that has helped make this project a really fulfilling one for me:
- John Longdong
- TANK8
- Modestyiswimpy
- Pufulet
- johnny moe
- Humin
- Jamesinator
- ScreechingEagles101623

Next, a big shoutout to the Hammer++ crew and for those who shared its release with me. Even though I only had the chance to use it for the last few beta versions, it is a massive improvement to the Source 1 Hammer editor, and brings it up to modern standards. Considering how out of date and broken the original Hammer Editor has been for the longest time, it's incredible to see such improvement on (what I assume) a closed source tool. I wish I had this a long time ago, but now I'm actually looking forward to working on more maps with this tool. Please show them some support!

When I started on the original versions of this map, I had a basic understanding and working of some of the tools for texture creation and management. With the later versions, I got more interested in trying to make my own custom textures, logos, designs, and try and incorporate them in a way that fit in and wasn't too immersion breaking. Here's some of these tools listed out below:
 - Inkscape
 - GIMP
 - Audacity
 - textures.com
 - VTFedit
 - GCFScape
 - Pakrat

### Thanks for reading! Enjoy the map and let me know if you end up making new map variations with the files provided! Feel free to add me on Steam to get in touch

### [back to top](/index.md#gm_scrapmetal_v5-final-edition)
