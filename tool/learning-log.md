# Learning Log 1

## Tool: **Kaboom**

## Project: **2D platformer game**

---

### 10/23/24:
#### What I first did
* Went the the kaboom (website)[https://kaboomjs.com/]
* scrolled around for abit at the website and read a bit
* looked at the [playground](https://kaboomjs.com/play?example=add)
* Wondered how I was going to code this then I realized I could just copy and paste the code and watch the tutorials
  #### Testing out the products of the tool
  * I went to the play ground and played some games to get an idea of what it is capable of
  * I played a rpg game, a flappy bird game, and also a jumping platform game

### 10/24/2024:
#### Researching my tool
* I watched this [kaboom video.](https://www.youtube.com/watch?v=iRXI6ThRJvM&list=PLNwtXgWIx3rgk68WwrykC7BIJ50kT6ZpS)
* Asked myself how I was going to make a pixel based gamed?
* Looked at more videos and read a bit of the [tutorial](https://kaboomjs.com/doc/setup)


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
# Learning log 2
## Tool: Kaboom
### Project: 2d platformer
11/2/2024
## Very simple testing/ examining
#### Very basic tinkeering with my tool and exploring parts of the play ground. Date 10/28
* I went to the [playground](https://kaboomjs.com/play?example=add) and started adding some sprites
* I added some sprites like ghost and realized you needed this code `loadSprite("bean", "/sprites/bean.png")` to be able to add a sprite.
* I then went to the [movement](https://kaboomjs.com/play?example=movement) part of the playground and changed the movement keys from arrows to WDSA keys.
* I also deleted some lines like `onKeyDown("up", () => {player.move(0, -SPEED) })` and the character stoped moving down so these must be a movement control.
#### Examining the RPG part of the playground
* I went to the [RPG](https://kaboomjs.com/play?example=rpg) section of the playground and there I examined everything first
* I changed the dialoge to "EEEEEE"
* Wondered how I can get the character to hold a weapon?
*  I was confused by this when I first saw it, but then I realized that It is the map.


 ````   const levels = [
		[
			"===|====",
			"=      =",
			"= $    =",
			"=    a =",
			"=      =",
			"=   @  =",
			"========",
		],
		[
			"--------",
			"-      -",
			"-   $  -",
			"|      -",
			"-    b -",
			"-  @   -",
			"--------",
		]
	]
````
# Learning log 3
## Tool: Kaboom
### Project

11/20/2024
## Tinkering the 2d platformers
 
  ### Going to double jump
* Went to [double jump](https://kaboomjs.com/play?example=doublejump) section to see the jumping that kabooms offers
* Scroll around for abit
* Notice the code block below along with `
````js
const PLAYER_SPEED = 640
const JUMP_FORCE = 1200
const NUM_PLATFORMS = 5
````
* I also saw a bean function that had ` body({ jumpForce: JUMP_FORCE }), doubleJump()` and then knew how to jump.
* Then I tinkered abit, changed the jumpforce to 2000 and I was done.


# Learning log 4
## Tool: Kaboom
### Project: 2d platformer rpg

12/3/24
#### Doing some final basic tinkering/reaserch before putong my tool in the ide

* Went to [youtube](https://www.youtube.com/) to reaserch for kaboom one last time
* Went the the [playground](https://kaboomjs.com/play?example=gravity)
* Tinkered on spriets and added dinosaurs and even made them  hostile
* Went to the rpg and made a unique level to refresh my knowlage on the tool
* Went to ai and made multiple mods

  #### The maze, final tinkering before putng kaboom into my ide
* Went to [maze](https://kaboomjs.com/play?example=maze) and looked around for abit
* Was abit overwehlem my the long wall of text.
* looked at functions like `function createMazeLevelMap(width, height, options)` I also noticed below that they are  sybols like "-", "┛", etc.
* I assumed that was used to make the map.
* I then decided to chek it out later as it felt abit complex for me, or I was to tired at the time (It was 9 at night)


  # Learning log 5
  # Learning log 6
  # Learning log 7
  # Learning log 8
    * Decided it was time to put Kaboom into my IDE 3/0
        * Ask my friend for help
        * My friend sends me to the [Kaboom tutorial](https://kaboomjs.com/doc/setup)
    * Go to my IDE
       * put `npm init kaboom -- mygame` into my tool bar
       * It doesen't work so I try it again
       * It works some how
       * put `cd mygame` into my tool bar
       * put `npm run dev` and now kaboom runs
         
      
  # Learning log 9
  * Now add a platform into my IDE
    * Go to [kaboom playground](https://kaboomjs.com/play?example=add)
    * Go to the platform section and examine it's code
    * Copy it code and put it into mh IDE
  * Open my notes
  * Write down that `loadSprite` loads all kinds of things like grass and beans
  * Write doen the `setGravity` sees how far you can jump
  * `Background` of coruses sets the background and it works like color.px. 
