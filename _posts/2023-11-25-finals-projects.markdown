---
title: "Assembly and a Bank Management System"
---

We had our finals just around this month. It was a bit hectic considering the rushed academic calendar but we got through. For me, the projects weren't too hard but it may be understandable if others don't have the same sentiment.

## Bank Management System
In our Object-Oriented Programming Class, we were tasked to essentially create a complete program that should be able to function within the desired criteria given per group. For this one, we could have up to four members, but I only made a group of two. I could've technically done it all but the assistance was worth it. This is because they were the one assigned to edit the video for our presentation and I also let them speak more than I have in our presentation. 

We were assigned to make a bank management system on a console or terminal environment only. We ended up making a system that is basically a state machine. Because of that, you can easily add or remove a transaction at any point in time in the history and it will recalculate correctly the balance in your account following whatever rule of the transaction is. This is possible as we don't store the end result of a transaction, rather we store the transaction itself and apply it in sequence from the initial state to get to the nth-state. For the display, it uses curses for a modern way of interaction within the console. This means there are menus, popups, dialogs, input fields and so on that really makes the interaction nice; all within the console. 

## This is a video of the menu
<video style="width: 90%;" autoplay controls>
  <source src="/assets/videos/bank-management-system-menu.mp4" type="video/mp4">
</video>

## This is a video when using it
<video style="width: 90%;" autoplay controls>
  <source src="/assets/videos/bank-management-system-inside.mp4" type="video/mp4">
</video>

## Assembly
In our Computer Architecture Class, we were tasked to simulate how "pipelining" improves efficiency in our programs (and the CPU) using some sort of assembly language. We used the MARS MIPS simulator environment for that. I made several programs that applies the concept of "pipelining" in different ways to show its efficiency. Although programming in assembly might be daunting, the MARS MIPS environment is way friendlier. But at the same time, I understand that a lot of my batchmates would struggle with it as they aren't as proficient yet in programming even in modern languages so expecting that they could translate much logic to a lower-level is being quite idealistic. Regardless, my group finished the tasks with me doing the programming and simulation; while my groupmates complete the paper.