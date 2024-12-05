# Entry 1
##### 11/4/24

## Greetings
 Hello, I am Fatjon and I am currently making my freedom project about me creating a RPG/ 2d platformer game using the tool [kaboom](https://kaboomjs.com/).

## Deciding my project
At first I had no real idea on what my project would be about, would it be a game, a soundtrack, a engine, etc. They were alot of ideas on what to do. But all I wanted to do was make a much better project this year then last year. Last year I waited until the last minute to do it and was lazy with it. I did not want a repeat of that shame  and I want to feel like I did as much as I could, but I still had no clue on what to do. I then decided that I was going to talk to a friend on what my idea should be something I never do since I do my work by myself , he told me that it should be a fun project that you will enjoy making so you do not get bored. I agreed with him so after brainstorming on what I like and could use as a project, I decided to go with video games. 


## Deciding my Tool

  Now I had to chose a tool and after careful thinking and thought on which tool I should chose I decided to go and use [kaboom](https://kaboomjs.com/) because it is designed for my project. As for my project I plan to make a 2d rpg video game that is similar to the [first zelda game](https://youtu.be/6g2vk8Gudqs?si=ek4g_W8S7XdAr9ce) where you can fight mobs, talk to npcs, and even explore the world because it seems like a very fun idea. It is not unique  or original, but competition breeds improvement. How I made sure it was the right tool for me was by looking at the rpg section to see what kaboom is capable of in this genre of video games and it did not disapoint. It was a great rpg and way to make my project, it had dialogue, items, and npcs, so it seemed like it was the perfect tool for my project.
  
  ## Researching my tool/ what to do diffrent this time
 For me reasearching my tool, I decided not to go on goolge this time, but insted go on youtube and type "Kaboom.js guide" to learn about it more. I also decided to read some of the kaboom parts to like the [tutorial](https://kaboomjs.com/doc/setup) and it was very tiring, but I kept reading certian parts of over and over again until I had gotten a decent understanding of what kaboom is about and how it operates. I had spent 5 hours reading those text.

## Testing out kaboom.js/ Content

 ### Basic tinkering and discovering
  How I began testing my tool was by going into the [kaboom playground](https://kaboomjs.com/play?example=add) and examining the code that was given. The code had given 4 sprites, 3 ghost and 1 bean. The code had these lines which load the sprites for the game. The second secton of code adds the sprite to a specific location. For this part, I wanted tochange the bean sprite into another sprite.
  ##### Pre 1st Tinker
  ````js
loadSprite("bean", "/sprites/bean.png")
loadSprite("ghosty", "/sprites/ghosty.png")

const player = add([
	sprite("bean"),   // sprite() component makes it render as a sprite
	pos(120, 80),     // pos() component gives it position, also enables movement
	rotate(0),        // rotate() component gives it rotation
	anchor("center")
 ````
##### Post 1st tinker

 I just decided to replace the bean with dinosaur to see if anything would happen, the reason I wanted dinosaour is because I wanted to see if I can a dinosaur sprite because I plan to use dinosuars in my final product as a mob. I also learned these things, `LoadSprite` loads a sprite, `pos` puts the sprite in a position, `rotate` as the name suggests, rotates the sprite, and `anchor` puts anchors the sprite into a state were they stay in place. After 
````js
loadSprite("dino", "/sprites/dino.png")
loadSprite("ghosty", "/sprites/ghosty.png")

const player = add([
	sprite("dino"),   // sprite() component makes it render as a sprite
	pos(120, 80),     // pos() component gives it position, also enables movement
	rotate(90),        // rotate() component gives it rotation
	anchor("center"), // anchor() component defines the pivot point (defaults to "topleft")
])
````
##### Pre second tinker

   After that I was thinking were to go next, so I talked to the classmate next to me on what part I should do next and I told him I was thinking of the movement section. He said to try out the ai part of kaboom as the ai mobs or npcs are very important for a rpg game. I llistened to him and went to the [ai section of kaboom](https://kaboomjs.com/play?example=ai) and was given two sprites, one being a bean/the player which you can control with the arrow keys, then a ghost sprite that shoots a projectile at you and follows you around.
   ````js
const SPEED = 320
const ENEMY_SPEED = 160
const BULLET_SPEED = 800

state("move", [ "idle", "attack", "move" ]),

enemy.onStateEnter("idle", async () => {
	await wait(0.5)
	enemy.enterState("attack")
})]
````
  ##### Post second tinker  
 For my tinker I wanted to make the bullet go very fast, to not be able to dodge. So after looking around the entire code for abit, I noticed the `const SPEED`. The speed command is used when you want to input a certian speed for a certian thing, like the code gives 320 speed for us. Anyway not that I knew this, I decided to change speed from 800 to 2000, then to 3000, until I decided to stop at 5000 because I already got the gist of it. 

 ##### Post Second tinker: part 2
 But after that I wanted to see if I could make the normally hostile mob into a friendly or neutral mob. So I decided to look at the `enemy.enterState` and looking at the commets left and made come to the conclusion that `.enterState` or `.onState` are commands that direct on what a mob does. So I just changed that "attack" to "idle" and it was no longer attacking me. I also deleted "attack: on the array for extra measure. So here is my final code
````js
const SPEED = 320
const ENEMY_SPEED = 160
const BULLET_SPEED = 5000

state("move", [ "idle", "move" ]),

enemy.onStateEnter("idle", async () => {
	await wait(0.5)
	enemy.enterState("idle")
})]
````
 
       
  ### The RPG section 
  But after my first tinkering and my second I then decided to go to the [rpg](https://kaboomjs.com/play?example=rpg) section. In the rpg section I first did acouple of tinkering in like change the dialoge using `dailog.say` and the already giving dialoge functions and that.  But this time, I did not want to just tinker and edit, I decided that I wanted to add something. I wanted to add another area of the rpg.However here is the problem, I did not know how. So the very first thing I did was the examine the code to see what would be helpful in solving the problem and I saw this block of code.
 ````js
const levels = [
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

  This section of code with the `const level` and just below it having the lines of code like `addlevel` or things like `"$","-","=","|"` made me think that you need to align the symbols a certian way or the way you like to make a level. So I coded this as my prototype map and I wanted to test it to see if it would work successfully.       
  ```js
           [          "---------------------------",
			"-                      -",
			"-   $                -",
			"|                  -",
			"-      @         -",
			"-       b     -",
			"=============",
		]
   ```

   My prototype as a successful and working fine. After this I decided to add abit more small things that add personality, this below was my final code, a completed and fully functinal level for you to see.
```js
const levels = [
		[
			"===|====",
			"=      =",
			"= $    =",
			"=    a =",
			"=      =",
			"=   @  =",
			"========",
		],
                  [   "---------------------------",
			"-      - -  =     -",
			"-   $  ---  -    -",
			"|      - -  -    -",
			"-      @         -",
			"-       b     -",
			"=============",
		],
		[
			"--------",
			"-      -",
			"-   $  -",
			"|      -",
			"-    b -",
			"-  @   -",
			"--------",
		],
	]

```
[Next](entry02.md)  

[Home](../README.md)
