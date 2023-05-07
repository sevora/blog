---
title: "I Developed 2 Applications in a Week"
---
So it's been months since my last post and I've been quite busy. Fortunately, as of the moment of writing, finals just ended and we are on break from college. For the finals, I developed two different applications for two different subjects.

## First Application: TodoPlusGPT
If it isn't obvious from how I named a project it is essentially a todo list powered by OpenAI's GPT models. I finished the whole working prototype in 3 days. Although it is lacking in the animation department which I believe would make the application feel much better. As in having page transitions and all that stuff. Still impressed that it works. 

On the very first version, I basically used the model to generate the whole result in JSON all at once. It was not an ideal solution. Sometimes it works, sometimes it doesn't. This is because the JSON is occassionally malformed considering that GPT models don't have the power to be completely deterministic upon its own choice. So generating the whole output I need all at once wasn't ideal.

Of course, I wanted it to be more robust and I updated it a bit. It should now use multiple queries and get the data chunk by chunk. Since the JSON output is considerably smaller, it may make less mistakes in formatting. But that isn't the only benefit. If a JSON output is malformed, it can skip that and go to the next query.

I heard from someone in our college, that we're going to have an application development subject anyways. That also means that I could use this project for that subject. I just have to make improvements. I guess I'll open source this very project **but only** after my application development subjects are done just so I could prevent potential problems. I mean, the professors might think I just copied the entire codebase from somewhere even though I'm the author from that somewhere.

## Second Application: Soundboard
This was a less exciting project and we were forced to employ a backward problem-solving method. *What do I mean?* Well, the subject here is programming and data structures, but it was more or less basics of programming and not much data structures. The task was to employ everything that has been taught or lectured during the course of the entire semester. The issue is, in software engineering, we only have to utilize what is necessary. There is a great danger in overengineering. 

We had no choice but to utilize these (the programming language used in the subject was Java): Lists, Sets, and Arrays. Another condition was that there had to be a 2D Array of Object References. I don't even use 2D arrays that much, and if I do it's only for primitives. Also, we can pretty much turn any array with n-dimensions into a single-dimension. So there's not much need for 2D arrays, it's needless complexity. If you do need one, you would want to wrap a 1D array instead and then emulate 2 dimensions. That's cost effective.

Overall, I wasn't excited for this project due to the conditions. But my output was decent. It's great that I made something a few years back and I could tweak that a lot in order to change the entire thing but have the same tech stack which already has the graphics and architecture set up.