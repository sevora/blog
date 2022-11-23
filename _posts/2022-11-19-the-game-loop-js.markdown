---
title: How I implement Game Loops in Javascript
---

This post leans on the technical side of things. This post will touch upon an implementation of how
a game loop, the loop that dictates when the logic update step and the visual rendering is run.

## So what is a game loop?
When we play games, we can easily split two main processes that occur repeatedly within the game.
That is, the logic updates of the game, and the rendering of graphics as a visual representation to that logic.
In the browser, we can use the built-in method `requestAnimationFrame` of the global `window` instance. The method 
accepts a callback function, where that callback function is run right before the next browser repaint.

## How to implement one?
The most basic implementation of this game loop would be as follows:
```js
function gameLoop() {
    window.requestAnimationFrame(gameLoop);
    update();
    render();
}

function update() {
    // code for updating logic
}

function render() {
    // code for rendering graphics
}

gameLoop();
```
But you would realize right away that you have no control over how many frames per second it runs. It would always run
as fast as it could. When developing games, a constant framerate is pretty important in other to keep the experience 
smooth, meaningful, and consistent. This is especially true for real-time games that require timing and precision.
Say, someone playing a platformer wouldn't want a sudden change in the game's speed as that will throw off their movement.

## How I implement mine?
Well, the big issue with the first implementation is having no control over the fps. So, modifying the game loop just a bit would
allow us to solve that problem:
```js
let now = Date.now();
let then = now;
let fps = 60;

function gameLoop() {
    window.requestAnimationFrame(gameLoop);

    now = Date.now();
    let elapsed = now - then;
    let interval = 1000 / fps;

    if (elapsed > interval) {
        then = now - (elapsed % interval);
        update();
        render();
    }
}
```
The implementation is relatively simple and is actually straightforward. We keep track of the time when the previous frame occurs,
we also keep track of the time the current frame occurs. We then want to only run the update and render step if the elapsed time necessary
is reached. The time is in milliseconds hence the interval is calculated with `1000 / fps` and in a 60fps game, every 16.67ms, the game would
update and render. 

The only confusing bit would be the computation for `then`. At first glance, it seems that `then = now` would be enough. However, the slight 
offset in the calculation would have somewhat of a greater impact relative to how far you're counting it from. What this means for example is,
the browser is able to run at 60 fps, but we are capping it to 10fps. Since the browser would repaint every 16.67ms, the value of `then` would 
eventually lag off by 12ms. In one whole second it would lag off a total of 120ms. Hence, `elapsed % interval` fixes that by making sure that the
`then` variable is set as an interval of the computed `1000 / fps` interval.

## That's pretty much it!
Go ahead, you can use this game loop on your HTML5 Canvas API projects.
