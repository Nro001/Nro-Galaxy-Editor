![icon](https://user-images.githubusercontent.com/107048186/183308766-ef93d871-3cb2-441c-b978-fff1da15a5dc.png)
# Stellaris-Galaxy-Editor
As a Type-5 Kardashev being, you are able to move the stars of a mere galaxy and manipulate their waypoints as you please with just a divine click of a button.

This is just a small project that generates visual map to edit the position of stars and connects/disconnects hyperlanes.

Note: I will be taking a break **now** as I have completed the main objectives. I just did this as a hobby ~~addiction~~ really and I'm in university so I need to focus with my studies. I just did this for fun during my summer break, by **"fun"**, I mean taking a month, usually full-time each session, of creating, coding and tweaking.

If there are any issues, post them [here](https://github.com/neroiii/Stellaris_Galaxy_Editor/issues).

Features
========================
- [x] Parses the _galactic_object_ of the save-file. Basically, stars and hyperlanes.
- [x] **Generate visual map for:**
- - [x] Stars: different visuals for _star_class_ and some modded ones
- - [x] Hyperlanes: bridge and `no bridges o_O?`
- - [ ] Wormholes: `Low-priority` There is an external section needed other than _galactic_object_
- [x] **Map Editor for:**
- - [x] Hyperlane: Connect/Disconnect
- - [x] Star: Input, Drag-Drop, Arrow
- - [ ] Wormholes: `Low-priority`
- - [ ] Delete Star `Mid-priority` Just use the Star-Eater for now, I guess?
- [x] Save feature `DONE` `Unoptimized`
- [x] **Miscellaneous**
- - [x] Toggle visibility for Stars, Names, Hyperlane
- - [x] Logs information to the DEBUG
- - [x] Flips the x-plane to imitate the map. *toggleable*
- - [x] Resume previous session, uses the original save-file. *toggleable*

Support
========================
**_I have seven cats, seven hells, help me buy cat food._**

Unfortunately, I can't make a PayPal account right now cause the validation ID seems to take a year to be processed and delivered t-t

Usage
========================
The save-file doesn't need to be a fresh start, it can be used any point in time of the game. The size of the save-file only affects how long it will take to process.

Initial
------------------------
Simply, run the application and drag and drop the `gamestate` file inside your save to the screen. If the application freezes, Lua is probably running the scripts. **DON'T FORGET TO CHECK THE DEBUG FOR THE STATUS**
* If you don't know how to get the file, you can go to the wiki for further instuctions: [Save-game editing](https://stellaris.paradoxwikis.com/Save-game_editing).
* Use [Notepad++](https://notepad-plus-plus.org/downloads/) if you want to open `gamestate` and save changes
* App Directory: `%APPDATA%/Stellaris-Galaxy-Editor/`
  * *If anyone has idea where they are in other OS please let me know*

Camera Controls
------------------------
* Movement: Keyboard arrows or `W` `A` `S` `D`
* Dash: Hold `Shift` to dash
* Zoom: Hold `Q` to zoom-out and `E` to zoom-in
* Reset: Press `R` to reset position and zoom
* Name: Hold `Alt` to temporarily show or hide star names 

Buttons
------------------------
There are three groups of button: `Visibility` `Edit` `Map` Hover to each icon to see their descriptions

* **Star Editor**: there are three ways to change their position and they are toggled by default
  * `Input`: Click the x or y input bar to change then press Enter. 
  * `Arrow`: Click the white cardinal arrows.
  * `Drag`: Click the star first then drag them anywhere. Negative values makes the drag smoother.     Range: 2 to (-3)
* **Hyperlane Editor**: click a star and another star to either connect or disconnect, automatically decides based on wether there is already connection. Click on the star itself if you want to cancel.
* **Miscellaneous**
  * `Flip`: map is inverted by default, so negative x is on the right side as to imitate Stellaris map. Toggleable
  * `Resume`: resumes previous session, the original gamestate. Does not resume any previous changes, if you want to update it, just drag another gamestate to the screen 

Saving
------------------------
To save the changes you have made: Simply click `Map`->`Save`. It will freeze the game as the Lua is running the scripts. This will take a bit of time, the more the save-file is larger. Check the DEBUG for status.
* The results of the changes are located: `.../save-file/packed/`
* There are two files you can choose that are created after you export:
  * `galactic-object-modified`: A more safer method. Using Notepad++ highlight the `{` in `galactic_object={` and press `Ctrl+Alt+B` then copy `Ctrl+C` then open your original gamestate (make a copy) and search for `galactic_object={` then highlight the `{` only and press `Ctrl+Alt+B` then paste `Ctrl+V` then save. Make sure "galactic_object={" is not duplicated.
  * `gamestate`: A less safer method. There's a "*Unicode error: invalid skip*" for this so I don't know if it might cause something but I tested this on a fresh save and it still works although there's a line on the error.log: "*Repaired savegame, cleared 11 invalid deposits!*."
* After that, open .sav file (make a copy) and paste the modified gamestate.

Changing to another save-file
------------------------
If you want to change to another save-file, simply drag your new `gamestate` to the screen
* If there is an error or bug, exit the application and open it again.
* If the application is set to resume the previous session, either delete `.../save-file/parsed` or go to the app directory `.../save-file/settings` and change it to `ResPrev=false`

Another way to edit
------------------------
If the application is too buggy for you and you have already generated a galaxy then set Resume=true then go to `.../save-file/parsed` and you can edit them manually using Notepad++.

The data's template can be translated as:
* `stars` : `ID`,`x`,`y`,`star_name`,`star_class`
* `hyperlanes` : `ID`,(`to`,`length`,`bridge`)

Open the application again, assuming resume is set to true, and then save, voilà!

Third-party software
========================
This project uses the following software:
* [Godot Engine](https://github.com/godotengine/godot)
* [Godot Lua PluginScript](https://github.com/gilzoide/godot-lua-pluginscript)


Changelog
========================
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
* Installed Godot Lua Plugin, rewrote my lua scripts
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
For a month now, I have coded all the basic features needed to edit star position and the hyperlanes from scratch. The only thing I'm lacking of is translating the Lua code I made for decoding and encoding, which might be another headache. Therefore, I will take a break from this after I complete my summer classes cause this is turning into my addiction.
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


* Cleaned the test files except for the saves, optimized decode and encode.
* Added else if statement because the string pattern matching goes bananas and decides to switch to another pattern type.
* Can read then write and replace.
* Positions can be changed, doesn't seem to crash but hyperlanes are an issue, they cause the crash on mass edit
* Now detects bridge=yes variable from hyperlane, (what are they use for??)

* I'll stop this for now, spent a week doing this, still have summer classes so, will take a break in a month


Alpha version: Roblox Studio
------------------------
My only intention was to visualize my map so I can edit them, now look what happend, I made this for a whole month and more and ~~more!~~...
