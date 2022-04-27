# Tower Defense, Platform Runner and Breakout Windows and MacOS Builds

Legends:
- Roshan Bellary - recklessHogrider96
- Marcin Kierzenka - mkierzenka
- Zachary Katancik - zkatancik
- Matin Raayai Ardakani - matinraayai

We designed and developed a Game Engine and used it to develop 3 different games.
The builds for each game are present in the bin folder of either the Windows or MacOS folder.

There is a level editor as well where the levels are all 3 above mentioned games can be found in the bin/editor folder.

## Tower Hour - Tower Defense

This is a 2D grid based Tower Defense game. There is a start and end in each level, the start is where the enemies begin spawning and the end is where they exit the map. Once they exit the map, the players health would reduce, which when it hits zero the level is lost. There is a currency system in game with which towers like, Rock Thrower, Archer Tower (Ranged) and Magic Tower (AOE), and mines can be bought to defend the exit. Upon killing each enemy, coins and score are earned using which more towers can be bought and placed in key places strategically. 

There are 3 waves of enemies in each level and a pause before the start of each level to strategize and take a breather. Clicking the Start Wave button on the bottom bar would start the wave. The enemies vary in health and the enemies spawned at the beginning of each wave are always lower health than the enemies spawned towards the end of the wave. In other words, enemies are spawned in order of their health in each wave.  

There are 4 levels in the game, in the order of increasing difficulty. The level editor can edit the following:
- Base underlying level - The light green background is the default upon with the path tiles can be placed.
- The spots where the towers can be placed in a grid fashion.
- The environment elements like trees, bushes, forests, stones in a free placement non grid dependent way.
- The number of enemies in wave for each level. The enemies shown in the editor are in order of their health, i.e, the first is the lowest health and the last is the highest health.

There is a Localization system built in as well with support for English (default) and Spanish. (It was a shortcut to add the map within the ResouceManager rather than create a txt file due to the lack of time to implement it and I never got around to refactoring it).

## Grave Runner - Platform Runner

Simple Platform runner game. 

Note for when you play the game: You can win the level without the key, by the way. The key would just increase the score.

## Breakdown - Breakout Game

Simple block breaker game with different types of blocks!

Note for when you play the game: Black bricks are walls, you cannot break them. The grey bricks are hard bricks and breaking it is optional to finish the level. But the more you break, the more points you get! 

## Level Editor - For all above Games

The Level editor edits the levels for all the three above games. Yeah I know that is incredible!

## Notes by each Legend.

### Roshan
- Rewrote level file design, generation and updation via level editor. Added Instructions menus. 
- Dynamic selection of block textures from the resources. Wrote backend for the level editor.
- Added Enemy Path file so that we can have pre defined paths as well.
- Added Enemy tower path to have layers levels.
- Built full Level editor.
- Built 4 levels. Wrote Enemy spawner and enemy spawner file with config data on what to spawn.
- Updated instructions.
- Built Level editor for Environment.
- The level editor would be able to edit 3 files at the same time, where all the information related to the layering in the level would be present.

### Matin
- Completely revamped how we organized levels and UI, making everything use the GameObject and Level architecture
and allow for reusable components across both games. This change allowed us to easily and modularly add buttons, UI elements,
and gameObjects in both the games and the editor. After the breakout game worked with the new design, others helped transfering
it into other deliverables of the project. I then helped each team member with bug fixes.

- Made delayed spawn component + other indicators used in the game logic. Made a separate enemy level file in sparse format.
Helped with bug fixes of other group members.

- Added Anti-tank mine. Helped with bug fixes of other group members. Ensured playability of previous components.
- Added level editor support for the enemy waves for each file.

### Marcin
- Mostly worked on porting over the GraveRunner functionality into the new infrastructure after Matin did the initial setup.
This included both the game itself and its level editor.
- Led the push to add the Rock Throwing Tower and support classes (E.g. Rock, RockThrower Component, etc.) including parsing level
files, creating the new objects, defining the interactions between Rocks and Enemies. Also did some touchups to
TdLevel/TdLogic-related code for handling the necessary new functionality (e.g. tracking score, lives, reducing enemy health, etc.).
Ported over and fixed unit tests for previous games. Added unit tests for the Tower Defense game code. Added documentation
throughout Tower Defense codebase.
- Added the health bars to enemies, put some time into investigating how to support tower upgrading. Then put some time into
making the submenu for towers and working with Zach to change their targeting preferences.
Also the usual small cleanups/touchups here and there.

### Zack
- Rewrote all UI components to be game objects, including buttons, menus, etc. Worked extensively
on game editors front-end to match rest of the component based architecture. 
- Did initial custom game setup getting a working game going from scratch, 
reconfigured the menus to new game, added UI elements to the in-game experience, and worked on grid components for object placement like mouse over of 
items when clicked.
- Added all new tower types with varying mechanics. Animated all towers and created sprites. Added 
ability for users to change the targeting of towers.
