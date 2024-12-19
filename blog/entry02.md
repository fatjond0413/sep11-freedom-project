# Entry 2
##### 12/18/24

## Content

   ## Some final tinkering of my tool
   I was tinkering with my tool kaboom for abit on the main website and after a while I decided that I should look around and get to know my tool abit more before I decided to import it into my Ide because I just wanted to make sure I knew how I was going to import a tool.. So I first look around on the [kaboom playground]() for abit and deciding on what to do. I went for the [flamebar section](https://kaboomjs.com/play?example=flamebar). There I was confronted with spining pinapple lines like those fire lines in mario. I first moved my arrow keys into the pinapples and I died. I then examined the code below and noticed the lines.
   ````js

function addFlamebar(position = vec2(0), angle = 0, num = 6) {
	const flameHead = add([
		pos(position),
		rotate(angle),
	])
	for (let i = 0; i < num; i++) {
		flameHead.add([
			sprite("pineapple"),
			pos(0, i * 48),
			area(),
			anchor("center"),
			"flame",
		])
	}

	flameHead.onUpdate(() => {
		flameHead.angle += dt() * 60
	})

	return flameHead
}

addFlamebar(vec2(200, 300), -60)
addFlamebar(vec2(480, 100), 180)
addFlamebar(vec2(400, 480), 0)

player.onCollide("flame", () => {
	addKaboom(player.pos)
	player.destroy()
})
   ````
  I see like lines `addFlamebar` and `player.destroy()` along with other lines of codes that I belive affect the pinable flamebar. I decided that I wanted to change the pinapple into dinosaures and make the flamebar faster. First I changed the `loadSprite("pineapple", "/sprites/pineapple.png")` into `loadSprite("dino", "/sprites/dino.png")` alogn with changing the `sprite ("pineapple")` to `sprite("dino")
  ````js
    for (let i = 0; i < num; i++) {
		flameHead.add([
			sprite("dino"),
			pos(0, i * 48),
			area(),
			anchor("center"),
			"flame",
		])
	}
  ````
AFter that I changed the location of the flame bar from `addFlamebar(vec2(200, 300), -60)` to `addFlamebar(vec2(480, 10), 180)` and I was done doing my final tinkering. Below is my final code or tinkered code is below
````js
function addFlamebar(position = vec2(0), angle = 0, num = 6) {
	const flameHead = add([
		pos(position),
		rotate(angle),
	])
	for (let i = 0; i < num; i++) {
		flameHead.add([
			sprite("dino"),
			pos(0, i * 48),
			area(),
			anchor("center"),
			"flame",
		])
	}

	flameHead.onUpdate(() => {
		flameHead.angle += dt() * 60
	})

	return flameHead
}

addFlamebar(vec2(200, 300), 860)
addFlamebar(vec2(70, 100), -60)
addFlamebar(vec2(400, 480), 0)

player.onCollide("flame", () => {
	addKaboom(player.pos)
	player.destroy()
})
````
   ## Brainstorming solutions on how to import tool kaboom into my Ide
   I first decided to look into my past [sep10 freedom project](https://github.com/fatjond0413/sep10-freedom-project/blob/main/index.html) as I had used A-frame on it, so that might help. But then I saw and remembered that I had forgot to put my tool in my freedom project. SO that was no help. After that I decided to put the entire code on the [add section](https://kaboomjs.com/play?example=add) of the kaboom playground in jsbin. Thinking the `kaboom()` would act as a importer. The code is below
   ````js
     kaboom()
loadSprite("bean", "/sprites/bean.png")
loadSprite("ghosty", "/sprites/ghosty.png")
const player = add([
	sprite("bean"),   // sprite() component makes it render as a sprite
	pos(120, 80),     // pos() component gives it position, also enables movement
	rotate(0),        // rotate() component gives it rotation
	anchor("center"), // anchor() component defines the pivot point (defaults to "topleft")
])
player.onUpdate(() => {
	player.angle += 120 * dt()
})
for (let i = 0; i < 3; i++) {
	const x = rand(0, width())
	const y = rand(0, height())
	add([
		sprite("ghosty"),
		pos(x, y),
	])
}
   ````

It did not work and when I tried as the console said that `kaboom()` was not definded. I did not really know what to do so I just decided to look on the [kaboom tutorial](https://kaboomjs.com/doc/setup). After scrolling for abit I noticed that on that on the top of the [tutorial](https://kaboomjs.com/doc/setup) it says that the most easy way to install kaboom.js. I looked at the section and it gave an indepth guide on how to import kaboom. They was alsoa [github repo](https://github.com/replit/kaboom?tab=readme-ov-file) that also gave in my opnion, a even better guide. After looking around for what do do I found these lines of code that are saying they will install kaboom.
````
$ npm init kaboom mygame
$ cd mygame
$ npm run dev
````
 But after a while, nothing had happened. It was tiring and I really wanted to give up as I felt like I was hitting roadblock after roadblock and geting nowhere. After that I decided to go on youtube again and I found this (video)[https://www.youtube.com/watch?v=hgReGsh5xVU] and it explained on what you needed to do to import kaboom. It also explained on how each line of code works like `import kaboom from "kaboom"` which imports kaboom.js or mabye `kaboom()` which initlizazes kaboom.js. But when I tried these lines of code along with adding sprites abd stuff. MY IDE had still not have imported kaboom. I inputed the code below into my IDE. At this point I had realized that they was no way I can do this by myself and I need some help from my teacher. 
 ````js
import kaboom from "https://unpkg.com/kaboom@3000.0.1/dist/kaboom.mjs";

kaboom();

add([
    text("hello"),
    pos(120, 80),
]);

 ````
## EDP
 In my EDP I belive I am at stage 3 and 4 as I have not even put imported my tool into my IDE yet and that is still a problem that I do not have a set solution on. But I am thinking of solutions on how I can try to import kaboom.js to my IDE. I also plan to ask my teacher on some support on this so I can get a better idea on how to takle this problem. After this, I should be on stage 4 with me being able to find a succesful way on how I can put my tool in my IDE. But that is for later. For now I am still on stage 3 and trying to import my tool into my IDE.

## SKills
The skill belive I am learning while doing myn sep11 freedom project is  collaberation because I show self-advocacy by going up to the teacher and asking for assisatace or a hint on how I can import my tool kaboom.js into my IDE and admiting that I will not beable to do this problem or import my IDE by myself. Another skill I belive I am learning or geting more experinced at is learning how to google as I had been learning how to search on youtube by typing "kaboom.js guides" or my going to the offical website, but at the tutorial instead. But my most prominat example is when I looked up "kaboom.js github" were it lead me to a gituhb guide with all of the lines of code. 
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
