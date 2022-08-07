![icon](https://user-images.githubusercontent.com/107048186/183308766-ef93d871-3cb2-441c-b978-fff1da15a5dc.png)
# Stellaris-Map-Editor (Work-In-Progress)

I just did this for fun, by "fun", taking a whole month and a whole day of just creating, coding and tweaking.
So, I will be taking a break and I don't know how If I can work at this at all, I'm just doing this as a hobby ~~addiction~~ really and my uni is nigh again so I need to focus with my studies.

Features
========================
- [x] Reads the `galactic_object` of the save-file
- [x] **Generate visual map for:**
- - [x] Stars: different visuals for unmodded `star_class`
- - [x] Hyperlanes: bridge and `no bridges o_O?`
- - [ ] Wormholes: another headache as it's not part of portion
- [x] **Map Editor for:**
- - [x] Hyperlane: Connect/Disconnect
- - [x] Star: Drag-Drop, Arrow
- - [ ] Wormholes
- [ ] Save changes from the map editor `NEXT GOAL`
- [x] **Miscellaneous**
- - [x] Toggle visibility for Stars, Names, Hyperlane
- - [x] Logs information to the DEBUG

Usage
========================
As of now the only function is to read and generate visual map, you have to manually edit the variables to your savefile.
For that, you have to get the `gamestate` file on your save, you can go to the wiki for further instuctions: [Save-game editing](https://stellaris.paradoxwikis.com/Save-game_editing). Drag and drop the file anywhere the application to start.

Third-party software
========================
This project uses the following software:
* [Godot Lua PluginScript](https://github.com/gilzoide/godot-lua-pluginscript) : Lua is necessary for my pattern-matching string functions.

Changelog
========================

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
