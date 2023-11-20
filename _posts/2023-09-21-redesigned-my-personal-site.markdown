---
title: "I Redesigned my Personal Site"
---
I am the kind of person who values putting things into practice rather than talking about them. Hence, instead of giving you these tech buzzwords and whatnot,
I'd just demonstrate to you what I can do.
Take a look [here](https://sevora.github.io/portfolio)!

## What's the purpose of that site?
I'd like to call it a portfolio site but it doesn't even showcase my works. Rather, it's just about me. So I guess, we can call it a personal site. 

The site doesn't totally reflect all of what I can do. It's just something for me to unleash my creativity a bit. I've probably done more complex things than that,
but most people wouldn't appreciate those complex things. They want shiny, showy things so that's what I played with.

## How did you think of it?
It's a website. It's 2023. We can do a lot of things with a website nowadays. I thought, *why not leverage that?*, though there are some issues: for one
a great desktop/laptop would have an easy time executing all the cool things even 3d models in the web, but phones, not so much. A lot of people are also on 
phones, so I shouldn't go crazy or all the flashy things won't be functional on a phone.

When I redesigned this site, I wanted something that's quite flashy, but is also feasible, or manageable for mobile devices. Hence this concept of having
a watch somewhere and it being the main control in a site is pretty interesting. I thought of putting the past and the present in two different sides of the page.

## How did you make it?
### Assets
For the main assets, I'd need a wristwatch and its hands as separate images having the same dimensions, lined-up perfectly. Thanks to my friend who's, at the time of
writing, exploring his life in Manila making good and bad decisions all the time, but is no doubt skillful at his work, made the wristwatch. Thank you Cy. I rendered
the images using the Canvas API but alas comes a problem.

The images weren't aligned.

This is where Daniel comes in and saves the day. He got the images and aligned them for me perfectly. Problem solved. Great work. Daniel is an aspiring animator fueled
by his childhood inspirations, although I would say there is some struggle when it comes to reaching his maximum potential, a lot of factors, he might just reach it one day. 

Anyways I got the images. 

### Programming
For this one, I managed my concerns by having them be in different files and then one index file that utilizes everything to put it all together. I wrote an "InteractiveWatch" class which would use the images and have the logic to be able to properly render the watch according to a given "unit of turns." It could also reset itself back to 0 instantly or in animated way.

Of course you had to use that class in a game loop, which would either cap at 60/120 fps depending on the device. For mobile, I set the limit to 60fps. Otherwise, it can go up to 120fps. For input polling I had to use several event listeners, as the events are different for mobile devices and desktops. However the positions to detect "turning the watch" are within the intervals of each "game update" regardless of how much the "touch/mousemove" listener runs. You just have to use atan2 on both the positions (translated to origin) to get an angle from said origin and then get the difference in angle between the latest and the previous position, which would tell us how much to turn the watch.

For the animations when you scroll into a content I made a custom solution which would basically check all elements with animations if theyre on the viewport or not. If they are, we apply the animation. There is just a problem with my original approach: it's very slow on mobile. Hence I did two things to make it way way efficient.

First optimization, is quite minor and simple really. We just add an interval in which the program should check for when an element with an animation reaches a viewport. The bigger it is, the lesser the amount of times we have to do collision checking between viewport and elements. But you can't set it too big otherwise it might not be able to detect an element at all.

Second optimization, a bit more complicated, is by using logic and assumptions. It's basically a tailored solution that works in this specific scenario. I wrote an efficient viewport "observer." Essentially, it works by having an anchor element which we assume is in the viewport, so it only has to check if the element before or after the anchor is in the viewport, and we can assume that every other element isn't on the viewport. We update the anchor accordingly to the neighbor which is in the viewport. Hence we have reduced possibly a lot of collision/viewport checks to only 2 checks at a time.

I also developed all this in Typescript and configured Webpack to bundle it all in a single `index.min.js` file. The type support is just significantly helpful and reduces the development time as we don't get lost in the codebase.

## That's it!
It's not too complicated if you would ask me.