VICTORIA 2 MAP MAKER TOOL MADE BY DOTDOT

Required files:		(place these in the same folder as the .jar)
	provinces.bmp
	state.bmp
	rgo.bmp
	liferating.bmp
	continent.bmp

Output files:
	Hopefully all nontrivial files needed to get the game to load the map, plus states, rgos, and life ratings.

It will take up to a couple minutes depending on your cpu.

Any province with a blue value of 255 in provinces.bmp will be considered an ocean province.
(The color of ocean provinces in the other bmp files is ignored.)
All others will be considered land.

State and continents will automatically be created based on the color of the province in state.bmp and continent.bmp. Same color = same state/continent. You can reuse colors you used in other files. For provinces that are colored with multiple colors then it will use the first color found which will be the top left most pixel of the province.

Life rating will be whatever the red value the provinces is filled with in the liferating.bmp.

The RGB colors for different rgos are:
	100	100 100 cotton
	100	100 200 dye
	100	100 255 wool
	100	200 100 silk
	100	200 200 coal
	100	255 100 sulphur
	100	255 200 iron
	200	100 100 timber
	200	100 200 tropical_wood
	200	100 255 rubber
	200	200 100 oil
	200	200 200 precious_metal
	200	255 100 cattle
	200	255 200 fish
	255	100 100 fruit
	255	100 200 grain
	255	100 255 tobacco
	255	200 100 tea
	255	200 200 coffee
	255	200 255 opium

If you crash before reaching the title screen something is probably wrong with your map files.
If you crash when pressing play something is probably wrong with your history files.

Referencing a nonexistant province, continent, state, etc in a decision, event, etc will crash the game on pressing play.
Use grep to search for them. For windows users baregrep exists.

rivers.bmp and terrain.bmp are made trivially in gimp using the fill tool and so this tool will not generate them for you.
Same goes for the dds colormaps in the terrain folder.
For positions/ports, use the Clausewitz Positions Editor.

Remember that you will need to change "definitions =" in default.map to include your mod name in the path. If you don't know what this means, look at other mods that edit the map in some way.

The empty vanilla province history files are apparently necessary. Not sure why, ask the TTA guys. A copy of these are provided and used by the program in the DONOTEDIT folder. (Temporarily remove all these empty province history files from your mod when using the Clausewitz Scenario Editor).

Your map files must have dimensions that are multiples of 144 or the game will crash.
