# Stellaris-Map-Editor (Work-In-Progress)

I just did this for fun, by "fun", taking a whole month and a whole day of just creating, coding and tweaking.
I will be taking a break and I don't know how If I can work at this at all, I'm just doing this as a hobby ~~addiction~~ really and University semester is nigh so I need to get serious with my life.

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

Third-party software
========================
This project uses the following software:
* [Godot Lua PluginScript](https://github.com/gilzoide/godot-lua-pluginscript) : for pattern-matching string functions.

0.9.2: Drag-drop savefile, read, parse, generate visual.

>Parses the contents of the star section of the save game using Lua since their string functions are crucial for pattern-matching.

>It can get most from elements to sub-elements either if it's used right now or not but I'm still confused why it can't get some things sometimes,  added contingencies as solution for necessary variables especially the [bridge] variable in the [hyperlane].

>Can drag and drop [gamestate] file to the executable to start the visual generation, so far it's the only way to initiate it.

>Added temporary icon

>No way to save the changes automatically yet, that's another headache I can't afford right now. Use this as a guide what to edit on your savefile for now.
>It's a mess of a code but no errors so far.

Merged too many
![Screenshot_4](https://user-images.githubusercontent.com/107048186/183307433-4008290b-4071-4eee-98f9-dba6cb04abb9.png)

0.9V: Optimized, will resume after I complete my summer classes
For a month now, I have coded all the basic features needed to edit star position and the hyperlanes from scratch. The only thing I'm lacking of is translating the Lua code I made for decoding and encoding, which might be another headache. Therefore, I will take a break from this after I complete my summer classes cause this is turning into my addiction.

>Optimized all code, by optimized, I compressed lines into a "for (key) in (array)" hell.

>Added ability to edit stars by dragging and clicking arrows

0.8V: Star Editor
It can now edit Star Position through input, It's already 4AM in my country and I'm still doing this thing while I still have freaking projects for the summer, I need help in addiction. I have basically finished all things I need to do for coding except for translating the Lua I coded  into this language. They complete the puzzle but they don't fit yet.

>Added ability to edit stars through coordinate input

>Added better UI button texture

 O.7V: Hyperlane Editor
 >Added buttons to toggle visiblity for names, stars and hyperlane

>Added the ability to add and remove hyperlanes
 
 0.6V: GODOT:
 After trying countless studios, I find it more comfortable to use Godot-Engine since I don't have to deal with problems that will take my focus out of the things I need to do especially with my measly coding skill.
 
 >Created a basic star and hyperlane generator
 
 >Created textures for the map,buttons and stars 

0.1 to >0.5V: Replit, Encoding and Decoding
##Old README##

PROJECT ON HIATUS, I HAVE SUMMER CLASS AND I SPENT A WHOLE WEEK PROCRASTINATING BY CODING THIS THING WHOLE WEEK
Possible problem: hyperlanes have bridge=yes variable now so I have to make a code that will cycle through it so I can remove it 

>Tested removing all the length on a savefile, it works but it turns into length=0 after looking at the map, might be used for distance travel?

>Cleaned the test files except for the saves, optimized decode and encode, however due to new codes added, I have to clean it later again, goal is to test if it works first.

![Untitled](https://user-images.githubusercontent.com/107048186/177850451-0274c56a-cdd4-4357-a741-e380f98c53d8.png)


>Added else if statement because the string goes bananas and decides to switch to another pattern especially %s+

>Can read then write then replace

>The replaced version works and does not crash anymore, although changing the values is not guaranted

>Positions can be changed, doesn't seem to crash

>However, editing hyperlanes is the issue right now since they cause the crash when I try to mass edit

>Now detects bridge=yes variable from hyperlane, (what are they use for??)

Project on hiatus, spent a week doing this, still have summer classes so, will take a break in a month

Problems with hyperlane still but the coordinates now work

alpha version: Roblox Studio, 
my only intention was to visualize my map so I can edit them, now look what happend, I made this for a whole month.


