---
title: "Starting to Appreciate C++"
---

When I started learning programming, I first explored different languages. I was curious as to what their differences
are. Of course, I quickly found out that their use case varied. One of the most important differences is if they are "low-level" or
"high-level."

## So low-level and high-level means...
Low-level doesn't mean that the language is for beginners, and that high-level is for experts. If anything, it's kinda the opposite.
The real definition of level in this context is how close it is to the hardware. A low-level programming language would be
very close to the hardware, meaning its features are quite tied to the very literal concepts such as RAM and memory usage.
It provides a level of control down to how many bits and bytes everything uses and so on. It is also quite hard
to do something in a low-level language that is relatively easy on high-level languages.

So high-level languages are quite closer to the human language, kind of. They also provide built-in functions that would otherwise be
tedious to do in low-level languages. They are also more liberal on how the programmer can write the code. Although that might sound good,
the degree of freedom high-level languages provide could be too much and easily lead beginners to bad practices such that they always write
crappy code. Things such as creation of GUIs, graphics-related concepts, would also be way easier on a high-level language than it is on a low-level language.
But there always is a price.

You see, we also have the terms *compiled* and *interpreted*. Low-level languages are usually compiled languages. A compiled language is converted to machine code,
essentially the very bits and bytes that would quite literally be put into the RAM and run. Whereas, high-level languages are usually interpreted. An interpreted language
has the instructions run line by line. Take a line in the code, run its machine code equivalent, and repeat for the next line and so on. That kind of process comes with an overhead.

A program that is already in binary can be ran directly by the machine. Otherwise, it would have to read in everything line by line, and translate to machine code equivalent every single
time. 

It is definitely easier to develop in a high-level language that is interpreted. But it comes with that performance cost.
One would not actually write a real-time game in Python even if it was possible simply because Python is amazingly slow. 
The same program written say in C++ could at least be 100x more efficient and faster by several magnitudes of order.

## So should I learn C++?
If you were to ask me today, I would recommend it. But thinking back when I was a beginner, I wouldn't.
While one could write blazingly fast and efficient code in C++, it is far from exactly being beginner-friendly. Add in all of the 
concepts one would have to actually learn related to logic and programming (regardless of the language used), it would be an extremely
tough time.

Back then, I really didn't care about the hardware, memory allocation and usage, I was more focused on the "logic" side of things and I didn't
want to worry about something that I still don't want to pay attention to. So I ended up using a high-level language, which is Javascript and learned a lot.
I then was able to go to Java and do some projects on it.

Now, I'm learning C++ and since I have the fundamental concepts down already on everything else, I now could pay attention to more complicated things to think about
which involves memory usage, allocation, and so on. The cool thing about C++ is you have a lot of control on how things work in your program. Though, a downside is
the development time of a software would also be significantly longer depending on how efficient you want the application to be. 

C++ also has a ton of features and I kid you not, I doubt anyone knows all of them and applies of those all at the same time in a single project. It takes a solid foundation
to even be able to tackle all of the things C++ provides and has. 

Well extra note: I would recommend [The Cherno](https://www.youtube.com/@TheCherno) if you wanna learn more about C++, as he really provides details on how it and the compiler works behind
the scenes which definitely helps in building an understanding of the language.

## So again should I learn C++?
If you're a beginner in programming in general. Maybe not. Though if you feel that your brain could withstand the equivalent mental damage of a tank shell being fired right in your face everyday, then 
maybe you could.

If you're quite advanced already in another programming language that is high-level such as Python or Javascript, YES. I would totally say that you should learn programming in C++. It's amazing what you could do 
with it. Also if you're mainly on Python, your program would be embarassingly slow anyways unless it uses libraries with C-bindings, which is technically just C run through Python which is still embarassing as 
Python on its own is slow and would not be viable if it weren't for that C-binding.

Okay, too much hate on Python. Whatever.

*Learn C++ if you think you could take it.*
