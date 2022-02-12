# gm_scrapmetal_v5 (final edition)

Welcome to the site / repository where I'm hosting the map files and assets used in gm_scrapmetal. There's a couple links and files scattered around so I'll sum up what's going on here:

- **Download Scrap Metal Valve Map Files (VMFs) and assets here**
- **Documentation of known issues and other info on the map files here**
- **Rambling retrospective and design thoughts below**
- **Resources used and Special Thanks below**

A quick summary: "Final Edition" just denotes that this will be the last major update and rework of the map. I'm happy to work with others and continue support if there are known issues or hotfixes needed, but from my personal experience, I'm satisfied with how this version of the map has turned out, and would like to move on to new maps and ideas. I'm hosting everything here in hopes it will be easy to download the map files and assets, and to share more information beyond just the Steam Workshop page.

# Rambling Retrospective and After Thoughts

I wanted to throw a little recap of some of my level design experience and personal learnings in here. I've talked and worked with a lot of people about level design in Source and it's always an intriguing topic for me. I'll keep this mainly on Scrap Metal's development, and maybe keep a bigger conversation going on another page later

## Getting started

To give a brief history of how I started with all this, I'll jump back to around 2010 or so. I frequented a Garry's Mod Zombie Survival server that had a large map rotation. I did enjoy a lot of the maps and they really did nail the feel of a zombie apocalypse (it helps with the theme of Half-Life 2 based assets and overall grunge feel). However, I felt there was a lack in variety, as you generally would find yourself barricaded in a big house, or some area taken from Half-Life and then reworked a little for gameplay balance. I decided around this time that I wanted to learn how to make my own maps to contribute and to have fun with.

## Inspiration

By around 2011 or so, I had gotten around with the basics of Source and Hammer (thanks to 3kliksphilip for his YouTube tutorials, very helpful as a beginner). Before Steam Workshop existed or was supported for Garry's Mod, there was a GMod built-in utility called "Toybox" that basically functioned in a similar way. There was also garrysmod.org which hosted a lot of addons in a more manual way as well. I released my first map on there (it wasn't very good but it got the basics out there), and after that I got more comfortable doing edits of existing maps to start.

Eventually, I did get around to creating a zombie survival map, zs_factory_v3, which was originally created by my dear friend Maria. I had the chance to expand it out a bit and improve some of the gameplay loop. It was generally well received (from what I could tell at least), and I had some more confidence to try and make something from the ground up.

At around this time in 2011-2013, there were probably 2 main games I was playing. Garry's Mod, and Battlefield 3 (and maybe some Halo Reach thrown in there). Looking back, Battlefield 3 seemed way ahead in time in terms of graphics, sound design, and the overall gameplay feel. I was just a kid back then with an Xbox 360, and we would always hop on after school to get some more rounds in. While today I would say some of the "cinematic" effects (blue color correction, lens flares, etc.) are a bit overboard, it did help the game keep a unique feel that has aged really well (don't even get me started on Battlefield 2042). I thought, as something to kind of flip the script, what if I made a map that sorta captured some of that feel in GMod?

## Close Quarters

If you're familiar with Battlefield 3's DLCs, you may remember "Close Quarters", with a more infantry focused setting. While I mainly remember that DLC for Ziba Tower and Donya Fortress, there was another map I enjoyed called "Scrapmetal". And yes, this is where *some* of the inspiration for this GMod map came from, name included. In Battlefield 3, this map was set in a collection of warehouses and foundries in the middle of somewhere, with you the player shooting the place up, which had a lot of destructible elements and bridges to cross.

While you could remake that map straight from Battlefield 3 (and there is a wonderful TTT version that [author]() made [here](), I wanted to find some way to adapt it to GMod Zombie Survival, and make a somewhat more open map (this goes against a lot of the zombie survival gameplay loop, I later found out). So, with all this in mind, I opened up Hammer and started trying to make something out of it

## Greybox... or not

One thing every level designer should start with is a basic plan on what the map's theme will be, gampeplay elements, etc. I have to be honest, looking back as a software developer now to how I started out, I really was never a guy to plan things out or do any documentation. Yep, I just wanted to jump into the code or level design and start breaking stuff, and to some degree this worked out. But sooner or later, I discovered I would hit a wall and be stuck and not know what to do, or how to connect these two pieces together.

Greyboxing, or block outs, help define structure and a sense of direction on how you progress on the level. From what I've seen at least, all of the pros do this, and I highly encourage those who are starting out to allocate however much time is needed, to try and plan out the majority of the layout before diving into the fun stuff. This same kind of idea happens in software development, with scrum teams, architecture discussions, and agile planning. As you start detailing and working through, you'll quickly find that maybe you didn't like the area you had planned out, and you'll be able to adapt quicker and make changes on the fly if the layout design is guiding you along the way.

I'm not sure if anyone could tell, but when I started Scrap Metal's development, there was no plan, and no greyboxing or layout done ahead of time. You guessed it, I winged it and created and detailed each area individually. Then I somehow had to connect everything together, and make this map somewhat balanced for zombie survival (it did not turn out that way). This process, while immediately rewarding to see one area you worked on look pretty and detailed, led to a roadblocks and delays along the way. There was a lot of difficulty in figuring out how to where to progress next, and how to fit everything in, and if I had maybe planned the layout better, it could have been a little more cohesive.

## Spawning in

I'm now gonna talk about each building in Scrap Metal and the inspirations I may have had at the time. This is mainly for me to review my thought process and see where improvements can be made in the future. We'll start with the "Spawn room", a.k.a the big warehouse the player usually starts in (humans in Zombie Survival). Up until the final version, only the top floor of this warehouse was accessible, and the idea was to have a somewhat big, open warehouse as the player start to give a sense of what the rest of the map would feel like

I do remember distinctly for this spawn room, I referenced some real world pictures of abandoned warehouse, to try and capture that same, eerie feeling of being alone in one. Big windows give a view to outside and are the main light source. There's a water puddle on the ground to give some interesting reflection (I didn't bother adding a prop or source as to why water is there in the first place, immersion ruined!), and a couple of destroyed pieces of concrete. One set piece (and I got the idea from some HL2 mod I can't seem to find now) was the destroyed Combine helicopter through the roof. One thematic element I wanted to have was some clear connections and ideas that this was in the Half-Life 2 setting, and that the area would be a little battle-torn and run down looking

In terms of zombie survival gameplay, this room doesn't really do anything except give humans a safe place to spawn (I remember on my old computer spawning into a zombie survival map would usually take me into the middle of the game). There is one room that is potentially usable, although it only has 1 doorway and some holes in the roof. The elevator shafts in the back also did not open until wave 2, to give humans a chance to safely spawn in through wave 1.

In V4, I wanted to better utilize some of this space, or more accurately, the whole building. So I added a big open warehouse underneath, that is mainly empty to give players a build area in Sandbox. I also had what I dub the "Steam room", which is the room on the roof connnected to the elevator shafts, and contains some generators, pipes, and machinery. I also had the idea of having this as a HL2 resistance hideout, and have these little lambda marked areas scattered around

## atlantic building

## XCCR building

## Train depot / lab building

## Outdoor areas

## Final edition wrap-up

## Closing thoughts and future plans

## Resources used and Special Thanks

First up, I'll just start listing out a bunch of people that have provided helpful feedback, praise, bugs and issues needing to be addressed, and everyone that has helped make this project a really fulfilling one for me:




Next, a big shoutout to the Hammer++ crew and for those who shared its release with me. Even though I only had the chance to use it for the last few beta versinos, it is a massive improvement to the Source 1 Hammer editor, and brings it up to modern standards. Considering how out of date and broken the original Hammer Editor has been for the longest time, it's incredible to see such improvement on (what I assume) a closed source tool. I wish I had this a long time ago, but now I'm actually looking forward to working on more maps with this tool. Please show them some support!

When I started on the original versions of this map, I had a basic understanding and working of some of the tools for texture creation and management. With the later versions, I got more interested in trying to make my own custome textures, logos, designs, and try and incorporate them in a way that fit in and wasn't too immersion breaking. Here's some of these tools listed out below:
 - Inkscape
 - VTFedit
 - GCFScape
 - Pakrat


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kawoofish/gm_scrapmetal/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
