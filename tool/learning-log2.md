# Learning log 2
## Tool: Kaboom
### Project: 2d platformer

#### Tinkeering with my tool and exploring parts of the play ground. Date 10/28
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
