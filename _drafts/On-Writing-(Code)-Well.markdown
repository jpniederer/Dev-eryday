---
layout: post
title:  "On Writing (Code) Well"
date: 2017-6-4 18:24:00 +0000
categories: Programming
---

Programming is writing. Even though the code we write is processed by computers that are indifferent to our style, it's essential to take special care to write code that is clear and concise. Lately I've been looking into ways to improve my natural language writing. So far I've completed both *[The Elements of Style][style]* by William Strunk and E.B. White, and *[On Writing Well][oww]* by William Zinsser, and I'm getting better each day. The thought I kept having while reading, "it's amazing how much of the advice from Strunk, White, and Zinsser applies not only to writing, but also to writing code."

Sure, not all of the advice is applicable. It'd be crazy if every writing tip these classics offer up were relevant to writing code. English and <Insert Your Favorite Programming Language Here> aren't equivalent. Regardless of the differences between natural language and code, we should write with intention in the best way that we can. The end goal of anything we write is for it to be read.

The ideas that follow are taken from Zinsser's *On Writing Well*. I share some of Zinsser's best advice about writing. Each tidbit has additional comments about how it can be applied to writing code.

Simplicity
--------
Writers strive to produce clear and simple passages. It's common for professional's to make their writing intentionally opaque, "but the secret of good writing is to strip every sentence to its cleanest components" (7). The simpler the message, the easier it is to understand. The same is true for our code. Simple, understandable solutions that get the job done are just as effective as the impenetrable one that requires 10 interfaces, 3 classes, and its own DSL just to print "Hello World." Robust multi-class solutions certainly have places where they're the best tool for the job, but make it as easy to understand as possible. Rewrite it until the greenest developer you know can explain the solution to you.

Removing Clutter
--------

Unity
--------

Refactoring
--------
Writers constantly go between writing and rewriting. Rewriting is like the practice of refactoring code. Writers may not have all the cool dev-ops tools that we have to make rewriting less of a chore, but the process of iteratively improving a piece of work is every bit as grounded into the writer's toolset. "Rewriting is the essence of writing well: it's where the game is won or lost" (84). 

"You won't write well until you understand that writing is an evolving process, not a product. Nobody expects you to get it right the first time, or even the second time" (85). Great writers look forward to the opportunity to improve their work. As developers, we should push ourselves to refactor more and take pride in the write-rewrite cycle.

"...effortless style is achieved by strenuous effort and constant refining" (234).

Take From the Best
---------
"The trick is to study writers who have it" (238).

"Find the best writers in the fields that interest you and read their work aloud. Get their voice and their taste into your ear--their attitude toward language" (238). For code this could translate to reading the source code of your favorite open source tools or projects. Rewrite some of the code and get a feel for the syntax, understand each line of code. 

Producing Value
---------
"If your values are sound, your writing will be sound. It all begins with intention. Figure out what you want to do and how you want to do it, and work your way with humanity and integrity to the completed article. Then you'll have something to sell" (264).

Advice for Code Reviews
---------
"Clarity is what every editor owes the reader. An editor should never allow something to get into print that he doesn't understand" (292). The act of peforming a code review is similar to that of an editor reviewing a publication. Both the code reviewer and editor serve as a gatekeeper for the work to be accepted. The goal of the positions is to make the end product better. Allowing code into a code base that no other developer understands is a quick way to kill a project. As code reviewers we should hold each other accountable for writing code that is understandable. 


Towards Mastery
---------
There are so many other great bits from Zinsser that deserve to be shared. "If you would like to write better than everybody else," Zinsser writes, "you have to want to write better than everybody else. You must take an obsessive pride in the smallest details of your craft" (289). This advice maps directly to writing code. In order to write code well, we have to go deep into the details. Every variable, function, class, line of code needs to be reasoned out. All of these assets need to be brought together to form a cohesive solution.

The last, and maybe the strongest, message that Zinsser leaves us with applies to any skill. Zinsser wrote this passage while discussing how to deal with editors. Here you can substitute "editor" with boss, code reviewer, employers, or nobody. The points here capture the spirit of my Dev-eryday project as well as words can. I'll let Zinsser's words stand alone. "Take your talent as far as you can and guard it with your life. Only you know how far that is; no editor knows. Writing well means believing in your writing and believing in yourself, taking risks, daring to be different, pushing yourself to excel. You will write only as well as you make yourself write" (293).