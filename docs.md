### [back to homepage](/index.md)

# gm_scrapmetal_v5 Documentation for mappers

This is a quick documentation page I'm throwing together discussing helpful tips, known issues, my personal setup and configurations.

## Hammer(++)

95% of this map's development was done on the Vanilla Valve Hammer World Editor (which was a bit of a pain). Especially with this map, even just loading the map (and I have an above average PC setup) would take forever. For the final edition versions, Hammer++ got it's big update that everyone had been waiting for, and luckily switching to that was pretty simple. Head over to their website and download Hammer++ in the configuration of your choice (in general for GMod, you'll probably want to use Source SDK 2013 Multiplayer, if you don't have that installed you can get in the Steam Library -> Tools).

[Hammer++ Download page](https://ficool2.github.io/HammerPlusPlus-Website/download.html)

## Helpful tips

### Visgroups

If you open the map, you'll take one look at the 2D grids and wonder how the heck you can navigate or place anything. Visgroups, both automatic and user created, are super helpful in clearing things you don't need to see i.e. aligning world geometry without prop meshes getting in the way. Auto visgroups actually got an enhancement in Hammer++, and I've also created some user visgroups that helped me when I was creating. I'll list out a few of the important ones below:

![Visgroups](/img/visgroup.png)

- Vol Models
  - Show/hide volumetric light models. These tend to appear as big white light shafts in the 3D view and a bunch of planes in 2D view. Hammer++ will also dynamically update prop_dynamic colors, so you may not be able to view them easily in the 3D view

- Extra areaportals
  - Areaportal usage is done extensively for optimization. However, having too many areaportals can actually hurt performance, so I reduced a decent chunk before the final versions

- Sprites
  - In 3D view, sprites can be somewhat annoying visually, so I added a visgroup for them. Hammer++ has an auto visgroup for Sprites that actually works better than mine (keep in mind user created visgroups need to be updated when new entities are copied, cloning with the shift key should retain visgroups)

### Cordon tool

I wasn't very familiar with the cordon tool until recently, and it's been a big help for me. This tool basically allows you to cull and work on certain sections of your map, which not only cleans up some editing space, but also allows you to compile a working section of that map (without having to readjust skybox / leaks). On the old Hammer this became crucial because the map's 3D view could barely handle everything being rendered at once (I used to be on an old computer that was pretty slow).

![Cordon](/img/hammer3.png)

### Hammer compile configurations

Generally I'll compile on "Fast" and do a quick and dirty compile to check lighting and props, although Hammer++ lighting preview now drastically helps with that in-editor. The main thing I can throw out there is if you're on a final compile, or want to see how lighting is affecting static props, I would run with the 3 advanced static prop lighting commands.

`-StaticPropLighting -StaticPropPolys -TextureShadows`

Add these to your VRAD configuration and you'll get much more accurate lighting on static props. Scrap Metal extensively uses this to get proper lighting for pipes and props embedded inside geometry. Mainly because Source usually calculates a static prop's lighting based on the "origin" (in the Hammer editor, you'll see the XYZ axes coming out of a certain point). If you have a beefy processor and don't want your CPU at 100% slowing everything down, you can also set a thread limit so you leave some CPU left for multi-tasking

`-threads 12`

Hammer++ also fixes the tendency for the default Hammer compiler to freeze up during compile, which made it difficult to tell if anything was working or not. I've been raving about Hammer++ features in all of this, and I do recommend it at this time as it fixes a lot of bugs and issues that Valve has neglected to fixed

### Fun facts

I checked back at some old compile logs for the old versions (dated to Oct. 2014), and the map took around an hour to compile (this was on Final settings, static prop lighting). I was probably on some old Intel dual core system and it's a miracle I was even able to get anything out on that old computer. But hopefully those who try and compile this map for their own use won't have as much trouble as I did

### [back to top](/docs.md#back-to-homepage)
