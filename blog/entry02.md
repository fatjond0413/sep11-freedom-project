# Entry 2
##### 12/18/24

## Content

   ## Some final testing of my tool
   I was tinkering with my tool kaboom for abit on the main website and after a while I decided that I should look around and get to know my tool abit more before I decided to import it into my Ide because I just wanted to make sure I knew how I was going to import a tool.. So I first look around on the [kaboom playground]() for abit and deciding on what to do. I went for the 

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

It did not work and when I tried as the console said that `kaboom()` was not definded. I did not really know what to do so I just decided to look on the [kaboom tutorial](https://kaboomjs.com/doc/setup). After scrolling for abit I noticed that on that on the top of the [tutorial](https://kaboomjs.com/doc/setup) it says that the most easy way to install kaboom.js. I looked at the section and it gave an indepth guide on how to import kaboom. They was alsoa [github repo](https://github.com/replit/kaboom?tab=readme-ov-file) that also gave in my opnion, a even better guide. After looking around for what do do I found these lines of code that are saying they will instal kaboom.
````
$ npm init kaboom mygame
$ cd mygame
$ npm run dev
````
 But after a while, nothing had happened. It was tiring and I really wanted to give up as I felt like I was hitting roadblock after roadblock and geting nowhere. After that I decided to go on youtube again and I found this (video)[https://www.youtube.com/watch?v=hgReGsh5xVU] and it explained on what you needed to do to import kaboom.
## EDP
 In my EDP I belive I am at stage 3 and 4 as I have not even put imported my tool into my IDE yet and that is still a problem that I do not have a set solution on. But I am thinking of solutions on how I can try to import kaboom.js to my IDE. I also plan to ask my teacher on some support on this so I can get a better idea on how to takle this problem. After this, I should be on stage 4 with me being able to find a succesful way on how I can put my tool in my IDE. But that is for later. For now I am still on stage 3 and trying to import my tool into my IDE.

## SKills

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
