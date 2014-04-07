--------------------------------------------------
- Basic Constmaker
- flayedfocus 2013
--------------------------------------------------

--------------------------------------------------
- Overview
--------------------------------------------------
This is a tool for making the *_const.txt files that Wervyn's engine uses.
I created it so that I wouldn't have to spend so much goddamn time tagging art.
Use it at your own risk, I'm not liable for anything this does to anybody's stupid
fucking machine. I don't care if you get stuck in a loop and your cpu explodes or
Megazeux doesn't run it on your Nintendo DS or Commodore 64 or whatever fucking
stupid thing you run Megazeux on. 

I don't want your feature suggestions, I don't want your bugfixes for it, go
eat a dick and die.

--------------------------------------------------
- Usage
--------------------------------------------------
1. When you load the world, hit P to start.
2. The bar at the bottom shows the keys you can hit, and after you've clicked, the information about your block.
3. The first time you left click sets one point, the second time you click sets the other.
4. Hit A to bring up a viewport that shows where the piece of art "appears" relative to the player.
   Click to set it.
5. Next comes a viewport template that lets you drag the piece of art around to set the destination X and Y
   for the piece. Click to set this.
6. Next up, you're asked for a clip list. This means which part of the art is "see through" for the engine
   so that Wervyn's safe copy will set the right fg/bg colors when "rendering." Write this as a list of numbers
   referring to the position of the block in the art as a single integer, separated by commas.
7. Once you've done all of your selections for your piece of art, press C to commit them to the text file.

--------------------------------------------------
- Quirks/Notes/Behavior
--------------------------------------------------
constmaker.mzx looks for maps in ./data which means you'll want to copy it and associated files out of the util
directory and into the toplevel if you're using my altered-ass version of Wervyn's engine.

I zero the entire array of spots and blank the cliplist for every line when the world first loads and when
you hit N to create a new file. This means that you don't have to fill in every fucking spot (a lot of art
won't actually appear on the edges of the VP, you'll have to actually use the engine to see what I mean)

Right click at any point in the process will cancel what you're doing and reset all the shit you've clicked, but 
I haven't actually tested this thoroughly. You're probably going to get junk data. I don't care.

Wervyn's engine looks for dos/win text files. This means that you need the \r\n and not just \n on the ends
of the lines. If you modify the file by hand and resave it with just \n on the end of the line, your art
will NOT appear in the game.

--------------------------------------------------
- Credits
--------------------------------------------------
flayedfocus - interesting commentary and you know, the actual app/world/whatever you want to call it
Wervyn - for being a cool dude and writing a really badass fake 3d engine that gives me tingly man feelings
