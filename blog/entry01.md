# Entry 1
##### 11/4/24

## Greetings
 Hello, I am Fatjon and I am currently making my freedom project about me creating a RPG/ 2d platformer game using the tool [kaboom](https://kaboomjs.com/).

## Deciding my project
At first I had no real idea on what my project would be about, would it be a game, a soundtrack, a engine, etc. They were alot of ideas on what to do. But all I wanted to do was make a much better project this year then last year. Last year I waited until the last minute to do it and was lazy with it. I did not want a repeat of that shame  and I want to feel like I did as much as I could, but I still had no clue on what to do. I then decided that I was going to talk to a friend on what my idea should be something I never do since I do my work by myself , he told me that it should be a fun project that you will enjoy making so you do not get bored. I agreed with him so after brainstorming on what I like and could use as a project, I decided to go with video games. 


## Deciding my Tool

  Now I had to chose a tool and after careful thinking and thought on which tool I should chose I decided to go and use [kaboom](https://kaboomjs.com/) because it is designed for my project. As for my project I plan to make a 2d rpg video game that is similar to the [first zelda game](https://youtu.be/6g2vk8Gudqs?si=ek4g_W8S7XdAr9ce) where you can fight mobs, talk to npcs, and even explore the world because it seems like a very fun idea. It is not unique  or original, but competition breeds improvement. How I made sure it was the right tool for me was by looking at the rpg section to see what kaboom is capable of in this genre of video games and it did not disapoint. It was a great rpg and way to make my project, it had dialogue, items, and npcs, so it seemed like it was the perfect tool for my project.I also went to reserch on youtube insted of google to learn about the tool as having itn explained to you is better than reading it sometimes as I hav learned from A-frame were I probably should have watched some videos on it. Anyways the videos shows me that  it was perfect for making my freedom project.

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

 I just decided to replace the bean with dinosaur to see if anything would happen, the reason I wanted dinosaour is because I wanted to see if I can a dinosaur sprite because I plan to use dinosuars in my final product as a mob. I also learned these things, `LoadSprite` loads a sprite, `pos` puts the sprite in a position, `rotate` as the name suggests, rotates the sprite, and `anchor` puts anchors the sprite into a state were they stay in place. 
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
  ### The RPG section 
  But where I really put my tinkering and EDP to the use was at the [rpg](https://kaboomjs.com/play?example=rpg) section. There was the bases for my project. It had alot of things, but mainly dialoge, for this section I decided that I need to change the message an npc says from "Hi bean" to "hello" as I need to learn and hi was to basic, so first I decided to look around the code and I noticed two blocks of code that sayd `js onst characters = {	"a": {	sprite: "bag",	msg: "Hi Bean! You should get that key!"}`, and `js player.onCollide("character", (ch) => { dialog.say(ch.msg)`. So looking at these I thought that if i change hello to hi in the msg variable the dialogue will change as well and it worked when I tested the improved code ran perfectly and I did not really need improvment so I just showed it to the student next to me.
 
[Next](entry02.md)  

[Home](../README.md)
