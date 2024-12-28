<img src="https://user-images.githubusercontent.com/107048186/212237920-09d01e3c-0f46-4759-b3ae-d39c05d73383.png" width="250" height="250">

[<img alt="Donate" width="250px" src="https://github.com/Nro001/Nro-Galaxy-Editor/assets/107048186/4edb1609-e3d4-437e-8b43-43d34f293b16" />](https://ko-fi.com/O4O2UEDP5)

You can support me on Ko-Fi, this is also where I release any current updates.


**For anyone using v1.5 before, delete the files in `%APPDATA%/Nro-Galaxy-Editor/`**

# Nro's Galaxy Editor for Stellaris
As a Type-5 Kardashev being, you are able to move the stars of a mere galaxy and manipulate their waypoints as you please with just a divine click of a button.

This is just a small project that generates visual map to edit the position of stars and connects/disconnects hyperlanes. This is also my first project that I actually finished so if there are any issues, post them [here](https://github.com/neroiii/Stellaris_Galaxy_Editor/issues).

Note: I will be taking a break **now** as I have completed the main objectives. I just did this as a hobby ~~addiction~~ really and I'm in university so I need to focus with my studies. I just did this for fun during my summer break, by **"fun"**, I mean taking a month, usually full-time each session, of creating textures, coding and tweaking.


[`Features`](#features) [`Support`](#support) [`Software`](#software) [`Changelog`](#changelog) [`Instructions`](#instructions-and-usage) [`Troubleshooting`](#troubleshooting)
------------------------
[`Initial`](#initial) [`Controls`](#camera-controls) [`Buttons`](#buttons) [`Saving`](#saving) [`Changing`](#changing-to-another-save-file) [`Manual Edit`](#a-manual-way-to-edit)
------------------------

![square](https://user-images.githubusercontent.com/107048186/212534084-3a9ac24b-1a95-4ab4-975b-2f5fb42352ef.png)
![Screenshot (22)](https://user-images.githubusercontent.com/107048186/222201630-fc28dcfb-2594-4d9f-8f70-85018f5a61f2.png)


Features
========================
- [x] Parses the _galactic_object_ of the save-file. Basically, stars and hyperlanes.
- [x] **Generate visual map for:**
- - [x] Stars: different visuals for _star_class_ and some modded ones
- - [x] Hyperlanes: bridge and `no bridges o_O?`
- - [ ] Simulating borders `high priority` There is an external section so it might take long to code.
- - [ ] Wormholes: `low-priority` There is an external section needed other than _galactic_object_
- [x] **Map Editor for:**
- - [x] Hyperlane: Connect/Disconnect, Isolate
- - [x] Star: Input, Drag-Drop, Arrow
- - [x] Nebula: Include, Exclude, Move, Size `NEW`
- - [ ] Wormholes: `low-priority`
- - [ ] Delete Star `mid-priority` Just use the Star-Eater for now, I guess?
- [x] Save feature `DONE`
- [x] **Miscellaneous**
- - [x] Search function 
- - [x] Toggle visibility for Stars, Names, Hyperlane
- - [x] Logs information to the DEBUG
- - [x] Flips the x-plane to imitate the map. *toggleable*
- - [x] Resume previous session, uses the original save-file. *toggleable*
- - [ ] Mass editing `non-priority` Try to [manually edit them](https://github.com/neroiii/Stellaris_Galaxy_Editor#a-manual-way-to-edit) for now.

Support
========================
**_I have seven cats, seven hells, help me buy cat food._**

[<img alt="Donate" width="300px" src="https://github.com/Nro001/Nro-Galaxy-Editor/assets/107048186/4edb1609-e3d4-437e-8b43-43d34f293b16" />](https://ko-fi.com/O4O2UEDP5)

**Update: *I was finally able to make a kofi! also we have ten cats, three dogs now.***

Video Tutorial
========================
https://www.youtube.com/watch?v=pAMM_ObnhUs

[![Watch the video](https://img.youtube.com/vi/pAMM_ObnhUs/maxresdefault.jpg)](https://youtu.be/pAMM_ObnhUs)

Instructions and Usage
========================
The save-file doesn't need to be a fresh start, it can be used any point in time of the game. The size of the save-file only affects how long it will take to process.
Post your creations on the [discussions](https://github.com/neroiii/Stellaris_Galaxy_Editor/discussions)!

Initial
------------------------
Before starting your ~~shenanigans~~ divine intervention:
* You must use [7-zip](https://www.7-zip.org/) for opening the save-files.
* You must use [Notepad++](https://notepad-plus-plus.org/downloads/) if you want to open the files
* For further instructions on save files and where to locate them: [Save-game editing](https://stellaris.paradoxwikis.com/Save-game_editing).
* App Directory: `%APPDATA%/Nro-Galaxy-Editor/`


1. Open your `.sav` file and drag and drop the `gamestate` to a folder then drag that file to the screen or open it using the file explorer. **(You must put it to a folder, the application won't read the temp folder)**
   
3. Either way, the application will freeze as it tries to read the contents. ~Check the logs for their status.~

Camera Controls
------------------------
* Movement: Keyboard arrows or `W` `A` `S` `D`
* Drag camera: `Right-click`
* Dash: Hold `Shift` to dash
* Zoom: Hold `Q` to zoom-out and `E` to zoom-in (NEW: `Mouse wheel` now works too)
* Reset: Press `R` to reset position and zoom
* Name: Hold `Tab` to temporarily show or hide star names
* Cancel: Press `Esc` to cancel editor
* Scale UI: `Ctrl [+ -]`

Buttons
------------------------
There are three groups of button: `Visibility` `Edit` `Map` Hover to each icon to see their descriptions

* **Star Editor**: there are three ways to change their position and they are toggled by default
  * `Input`: Click the x or y input bar to change then press Enter. 
  * `Arrow`: Click the white cardinal arrows.
  * `Drag`: Click the star first then drag them anywhere. Negative values makes the drag smoother.     Range: 2 to (-3)
* **Hyperlane Editor**: click a star and another star to either connect or disconnect, automatically decides based on whether there is already a connection. Click on the star itself if you want to cancel.
  * `Isolate`: Click on any star to remove all of its hyperlane
* **Nebula Editor**: click a star or use the UI to add/remove them, you can also resize and move the nebula where you please. `NEW`
* **Miscellaneous**
  * `Search`: Can use ID or Star's name to possibly find what you look for, if an input exist, it will go to the first star found.
  * `Flip`: Map is inverted by default, so negative x is on the right side as to imitate Stellaris map. Toggleable
  * `Resume`: Resumes previous session, the original gamestate. Does not resume any previous changes, if you want to update it, just drag the saved gamestate.
  * ~~`Sandbox`: Turns the map into spiral~~ `DISABLED`
  
Saving
------------------------
To save the changes you have made: Simply click `Map`->`Save`. The application will freeze while it's packing the files, the larger the save is, the longer it will take. Check the Debug for status.

* The results of the changes are located: `.../packed/`
* Since there are difficulties in packing the file itself, two files are created instead as a result: `gamestate` and `galactic-object`
* These two files are methods on how you can put the modified gamestate:

  * `gamestate`: It is relatively safe now since I used a different way of saving it.

   **NOTE: This is before 3.3, `galactic_object={` is now `galactic_object=` new line `{` so searching is now `galactic_object=\n`**
 
  * `galactic-object`: A more safer method. Copy everything inside this file using Notepad++ then open your original gamestate (make a copy) and search for `galactic_object={`, highlight the `{` only and press `Ctrl+Alt+B` then `Ctrl+V` to paste what you copied before. Save and make sure "galactic_object={" is not duplicated and starbase_mgr={ is intacted. 

* After that whole debacle, follow these steps properly, make a copy of the .sav file you used, **DON'T ARCHIVE, MAKE A COPY** and open it using 7-zip and drag the modified gamestate there **directly**, the file must be overwriten to work and then bam! you're done! Congratulations, now the denizens of your galaxy are confused why their constellations have changed in just a day. Was there a large clusters of wormhole that transported everyone there? Did some shmuck invented teleportation and suddenly pressed the big red button? or is everything just a simulation? Who knows? **Maybe it has always been there. What was, will be; What will be, was.**

Troubleshooting
------------------------
**All the stars are gone! Why? Did the Prethoryn or Unbidden came?**

From my experience, there's three possible reasons for that

* You created/archive a new .sav file, it is not recommended as it would require following these [compression configurations](https://stellaris.paradoxwikis.com/Save-game_editing#Compression_on_Windows). You should only copy your .sav file, open it in 7zip and drag your modified gamestate there so it is overwritten.
  
* There's an error on how the *gamestate* was formatted, there was an issue with the double brackets `}}` instead of `} new line }`, as of the current version of this editor, it is now fixed but there might be mishaps similar to this, please create an issue.

   **NOTE: This is before 3.3, `galactic_object={` is now `galactic_object=` new line `{`**
* The `galactic_object={` is duplicated in which case it becomes `galactic_object=galactic_object={`, delete that duplicate. This usually happens when the contents of `galactic-object` is not copied properly, only highlight `{` and press `Ctrl+Alt+B` and copy.


**I can't click anything on the editor**
* Sometimes the entities are not deleted or replaced properly, just close the application.

If there are any other issues, please go to the Issues tab and post your problem including your modified gamestate file if you can.

Changing to another save-file
------------------------
If you want to change to another save-file, simply drag your new `gamestate` to the screen
* If there is an error or bug, exit the application and open it again.
* If the application is set to resume the previous session, either delete `.../parsed` or go to the app directory `.../settings` and change it to `Resume=0`

A manual way to edit
------------------------
**Note: This is still doable but the files mentioned here are now formatted in JSON**

If the application is too buggy for you, generate a galaxy on the application then toggle the [Resume] button or change the settings to Resume=1 then go to `.../parsed` and there you can edit them manually using Notepad++.

The data's template can be translated as: `file` : `attributes`
* `stars` : `ID`,`x`,`y`,`star_name`,`star_class`
* `hyperlanes` : `ID`,  (`to`,`length`,`bridge`)

*Note: new stars can't be added as it does not have an existing file on the unpacked folder and it is not advisable to delete them for now. 
Hyperlanes on the other hand, can be modified but you must add it on both IDs for it to work, it must be paired.

Open the application again, assuming resume is toggled, and then save again, voilà!

Software
========================
This project uses [Godot Engine](https://github.com/godotengine/godot) to create this standalone application.

Third-party software:
------------------------
~~[Godot Lua PluginScript](https://github.com/gilzoide/godot-lua-pluginscript)~~

~~[gdunzip](https://github.com/jellehermsen/gdunzip)~~


Changelog
========================

**2.0-Optimized**
------------------------
Notice: Not tested in-game since I've stopped playing for months, make an issue if there's another bug, the editor can read the modified save file so at the very least it should work.
* Fix another empty galaxy issue due to double bracketing bug
* Reduce memory consumption when saving -> less chances of empty gamestate. Who would have thought changing one method by chance would reduce the lag greatly.
* Added notice of the freezing when saving starts.

**Anyway, I still have no plans of working with this editor again, I don't have an incentive rn.**

**2.0-release: Nebula + Reworked UI**
------------------------
Woah, quite a jump in the version number there!

* Added nebulas to the map so now you can see which are included and how large it is
* Nebula Editor, including/excluding stars, change size and position of nebula
* Reworked the UI to pretty much look similar to baseline Stellaris
* Reworkd the appearance of star classes, now includes binary and trinary classes!
* File explorer added in the starting menu as an alternate to dragging the file.
* Search has now categories of star classes
* Improved searching algorithm, now includes stars with similarity
* Fixed numbers completely being rounded.
* Added [Controls] tab
* Added a guide to which star you are hovering
* Added sliders to some editors
* `Drag` - Right mouse button
* `Scale UI` - Ctrl [+ -] 
* Disabled Sandbox for now due to UI changes, you can use the previous version for it.
  
<img src="https://github.com/Nro001/Nro-Galaxy-Editor/assets/107048186/68924dc6-6a30-4370-9754-44c96df50ee2" width="575.21" height="337.8"> <img src="https://github.com/Nro001/Nro-Galaxy-Editor/assets/107048186/fb32ca6a-3049-44cf-95f6-4c0d644f5793" width="500" height="337.8">


  


**1.6-release: Fixed for 3.10x**
------------------------
It now works with 3.10x games, I might add new features like wormhole editing but I'm still too busy right now.

* Now works for 3.10+ Stellaris, they changed the format a bit, my code was specific on how it edits the variables so I had to change it.
* Added mouse wheel to zoom
* Tweaked Search feature
* Changed JSON to a format that isn't one-lined (didn't know it was possible)
  
**1.5-release: Sandbox**
------------------------
This might be my last big update for this editor, I'm too busy irl.

* Added Square Spiral and Ring maker
* Added Demo button on start screen
* Rewrote most of the code so it runs more faster now.
* Reworked some of the UI
* Switched to JSON format
* Removed Lua dependency and converted to purely GDScript
* Removed gdunzip

**1.1.0-stable: UI + Video Tutorial**
------------------------
I have been to busy with uni these days so I can't do any big changes with the editor

* Made the UI less crappy and added some small features
* Added much need information in the editor
* Made a video tutorial
* Updated README.md 

**1.0.0-stable: Hiatus: Search and Isolate Star functions added**
------------------------
My Uni officially starts this week so I won't be touching this project unless it's bug fixes.

* Search function: Uses Engine's String:Find function
* Isolate Star function
* Link Button to GitHub
* Fixed Camera boundaries due to [Flip]
* Changed [Info] to act like a tooltip
* Fixed starbase_mgr getting cut or missing from [gamestate] method
* Removed "galactic_object" from galactic_object-modified for convenience
* [Escape] key added to cancel Editor
* Fixed Hyperlane being on top of Star
* Updated README.md 

**1.0.0 beta-3: .sav file now draggable, output directory opens**
------------------------
Minor additions for convenience.

* [.sav] files or the save-file itself can now be dragged to the screen!
* The output directory will now open after saving is finished.

**1.0.0 beta-2: Minor fixes**
------------------------
Justtt a bit more dopamine.

* Fixed [Resume], now works properly
* Fixed clearing previous maps, made a better alternative.

**1.0.0 beta: It can now save!** Repository now public.
------------------------
Now I take a break.

* Added save feature
* Map is now inverted at x-plane by default as to imitate the galaxy map. *toggleable*
* Added a resume previous session feature, off by default
* Updated README.md

The coding is a bit of a mess, Function>>Optimize, but it works as intended.

_Fear the Blorg Aeternum!_

<img src="https://user-images.githubusercontent.com/107048186/183735974-93249845-a2a7-458e-95a5-b47e26544c30.png" width="631" height="384">


**0.9.2: Drag-drop savefile, read, parse, generate visual.**
------------------------
* Added [https://github.com/gilzoide/godot-lua-pluginscript](https://github.com/gilzoide/godot-lua-pluginscript), rewrote my lua scripts from scratch
* Parses the contents of the star section of the save game using Lua since their string functions are crucial for pattern-matching.
* It can get most from elements to sub-elements either if it's used right now or not but I'm still confused why it can't get some things sometimes,  added contingencies as solution for necessary variables especially the `bridge` variable in the `hyperlane`.
* Can drag and drop `gamestate` file to the executable to start the visual generation, so far it's the only way to initiate it.
* Added temporary icon for the application
* No way to save the changes automatically yet, that's another headache I can't afford right now. Use this as a guide what to edit on your savefile for now.
* It's a mess of a code but no errors so far.

_Merged too many savefiles in one, the parallel universes are merging!_

<img src="https://user-images.githubusercontent.com/107048186/183307433-4008290b-4071-4eee-98f9-dba6cb04abb9.png" width="420" height="355">

**0.9: Edit Stars by dragging and clicking and optimized all code**
------------------------
For a month now, I have coded all the basic features needed to edit star position and the hyperlanes from scratch. The only thing I'm lacking of is translating the Lua code I made for parsing and packing, which might be another headache. Therefore, I will take a break from this after I complete my summer classes cause this is turning into my addiction.
* Optimized all code, by optimized, I compressed lines into a "for (key) in (array)" hell.
* Added ability to edit stars by dragging and clicking arrows

**0.8: Star Editor**
------------------------
It can now edit Star Position through input, It's already 4AM in my country and I'm still doing this thing while I still have freaking projects for the summer, I need help in addiction. I have basically finished all things I need to do for coding except for translating the Lua I coded  into this language. They complete the puzzle but they don't fit yet.
* Added ability to edit stars through coordinate input
* Added better UI button texture, from scratch

**0.7: Hyperlane Editor**
 ------------------------
* Added buttons to toggle visiblity for names, stars and hyperlane
* Added the ability to add and remove hyperlanes
 
**0.6: GODOT:**
 ------------------------
 After trying countless studios, I find it more comfortable to use Godot-Engine since I don't have to deal with problems that will take my focus out of the things I need to do especially with my measly coding skill.
* Created a basic star and hyperlane generator
* Created textures for the map,buttons and stars 
* Moved to a different Github repository

**0.1-0.5: Replit, Encoding and Decoding**
 ------------------------
`##Old README##`
I HAVE SUMMER CLASS AND I SPENT A WHOLE WEEK PROCRASTINATING BY CODING THIS THING WHOLE WEEK

_Results of mass editing: changing the coordinates work but changing the hyperlane crashes_

<img src="https://user-images.githubusercontent.com/107048186/177850451-0274c56a-cdd4-4357-a741-e380f98c53d8.png" width="480" height="330">


* Cleaned the test files except for the saves, optimized parsing and packing.
* Added else if statement because the string pattern matching goes bananas and decides to switch to another pattern type.
* Can read then write and replace.
* Positions can be changed, doesn't seem to crash but hyperlanes are an issue, they cause the crash on mass edit
* Now detects bridge=yes variable from hyperlane, (what are they use for??)

* I'll stop this for now, spent a week doing this, still have summer classes so, will take a break in a month


Alpha version: Roblox Studio
------------------------
My only intention was to visualize my map so I can edit them, now look what happend, I made this for a whole month and more and ~~more!~~...
