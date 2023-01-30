---
title: "Back to Game Development"
---

It's been a few weeks since I added an entry. But now, I'm back. My best friend lent me this beast of a laptop so that we can continue game development and also for me to continue progressing while I'm saving up for my own setup.

Anyways, Godot 4 still ain't exactly out and that's what we're planning to use originally. We're hoping that the update will provide significant performance optimizations especially for the GLES3 renderer since on mobile it's still a bit heavy right now and our game requires at least a mid-to-high end phone. 

![A gif of one of the game scenes](/assets/gifs/back-to-game-development-1.gif)

## What are we working on?
Here's how it went.

I was using a pretty low-end machine on the initial stages of development. To get around the fact that we're gonna need to use heavy software mainly for the 3D side of things such as maps and models, I had to find alternatives. So, instead of using [Blender](https://www.blender.org) for the maps, I used [TrenchBroom](https://trenchbroom.github.io) which works. It's a software you can use to basically make maps for the old MS Windows games, or Source games, games that are similar to the classic DOOM and so on. The issue about this is development of mechanics such as moving platforms and more are gonna have to be implemented by me from scratch and I'm also restricted to GDScript for compatibility reasons. Hence, in GIF below is basically code I wrote just to have moving platforms, and it ain't even complete yet as it has no proper collision handling.

![A gif of one of the game scenes](/assets/gifs/back-to-game-development-2.gif)

Hence, every new mechanic or obstacle that we want would have to be implemented by me from scratch. Although Godot already supports basically what I want to achieve, I still have to write it from scratch as the map is made on TrenchBroom and it would be hardly intuitive to have to split the map editing process to two different softwares and having them mesh together would also be a hassle.

So, since I have a better setup as of this moment, the plan is to take a look at other game engines, preferably ones with an actual 3D level editor with them and migrate to them. Godot doesn't have a dedicated 3D map editor at all even though it supports 3D. So far the best candidate we have would be Unity. I'll keep this journal updated once more progress has been done. 

## To Cy
Thanks for this opportunity. I feel like I'm unrestricted now, that I can go exert more effort and the machine could keep up. Let's get this game going!