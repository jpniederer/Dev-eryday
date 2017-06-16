---
layout: post
title:  "On Writing (Code) Well"
date: 2017-6-4 18:24:00 +0000
categories: Programming
---

Programming is writing. Even though the code we write is processed by computers that are indifferent to our style, it's essential to take special care to write code that is clear and concise. Lately I've been looking into ways to improve my natural language writing. So far I've completed both *[The Elements of Style][style]* by William Strunk and E.B. White, and *[On Writing Well][oww]* by William Zinsser, and I'm getting better each day. Through my reading, the thought that kept coming to mind was: "it's amazing how much of this advice applies not only to writing, but also to writing code."

Sure, not all of the advice is applicable. It'd be crazy if every writing tip these classics offer up were relevant to writing code. English and <Insert Your Favorite Programming Language Here> aren't equivalent. Regardless of the differences between natural language and code, we should write with intention in the best way that we can. The end goal of anything we write is for it to be read.

All quotes that follow are taken from Zinsser's *On Writing Well*. I share some of Zinsser's best advice about writing. Each tidbit has additional comments about how Zinsser's idea can be applied to writing code. Many of the tips are common practices that most software developers are already following, but it never hurts to be reminded of such important tricks. If the tips are new, that's great, start putting them into practice and watch your work quality soar. Even if the tips don't make your software skills improve, perhaps they'll help your writing style.

Simplicity
--------
Writers strive to produce clear and simple passages. It's common for professionals to make their writing intentionally opaque, "but the secret of good writing is to strip every sentence to its cleanest components" (7). The simpler the message, the easier it is to understand. The same is true for our code. Simple, understandable solutions that get the job done are just as effective as the impenetrable one that requires 10 interfaces, 3 classes, and its own DSL just to print "Hello World." Robust multi-class solutions certainly have places where they're the best tool for the job, but make it as easy to understand as possible. Rewrite it until the greenest developer you know can explain the solution to you.

Removing Clutter
--------
If a word doesn't serve a purpose it should be removed. "Look for clutter in your writing and prune it ruthlessly. Be grateful for everything you can throw away" (17). It might be apparent already, but if Zinsser were a programmer he would not stand for having unused variables in his code. Don't get attached to any piece of code. Unused variables, outdated or excessive comments, and deprecated functions, and long forgotten classes are all examples of ways we clutter our codebases. With the power of source control, there is no good reason not to remove a piece of code as soon as it stops being needed. Every dead line of code increases technical debt and makes the system harder to support.

Write with Care
--------
"In terms of craft, there's no excuse for losing readers through sloppy workmanship" (26). Nobody likes to read shoddy work. It's not pleasant. Not only that, but sloppy code can make a simple task drag out into a long one. Finding bugs or updating a feature within careless code is a brutal chore. The best way to take care when writing is write your prose or code in a style that you would want to read. Try to make content that when chance brings you back to it you are glad to read it again. This will create a presence in your work that sets the tone for the output.  

This concept isn't just limited to our code. Developers often release tools for others to use. It's so important to help the user experience to be as easy as possible. Let's imagine two JavaScript libraries that can be used for time calculations. Let's call the libraries TimeCalc A and TimeCalc B. TimeCalc A has 100s of features but all of the examples are poorly documented and sample code rarely works. TimeCalc B has 20 features but has great documentation and each example has passing unit tests. TimeCalc A is going to lose its audience to TimeCalc B because it isn't as inviting. Taking care in your writing can enhance any software or tool you produce.

Unity
--------

Refactoring
--------
Writers constantly go between writing and rewriting. Rewriting is like the practice of refactoring code. Writers may not have all the cool dev-ops tools that we have to make rewriting a painless effort, but the process of iteratively improving a piece of work is every bit as grounded into the writer's toolset. "Rewriting is the essence of writing well: it's where the game is won or lost" (84). Just because a piece of code can pass its unit tests and work in production, doesn't mean that it's good code. That just means that it's *working* code. Working code is great but it's professional to write code that works and is supportable.

"You won't write well until you understand that writing is an evolving process, not a product. Nobody expects you to get it right the first time, or even the second time" (85). Great writers look forward to the opportunity to improve their work. As developers, we should push ourselves to refactor more and take pride in the write-rewrite cycle. 

"...effortless style is achieved by strenuous effort and constant refining" (234).

Take from the Best
---------
"The trick is to study writers who have it" (238). The internet is the best source to study such developers. GitHub is full codebases where many of the best software developers to ever live have posted their code for the whole world to see. Take advantage of this resource. There's also countless blogs where people are sharing their thoughts on the technical challenges they've solved. In addition to blogs, pick up books written by developers you admire. In addition to picking up tricks from the masters, you'll also support a creator who has impacted your life.

"Find the best writers in the fields that interest you and read their work aloud. Get their voice and their taste into your ear--their attitude toward language" (238). For code this could translate to reading the source code of your favorite open source tools or projects. You don't have to read their source code out loud, but there are many other ways you can aborb their knowledge. Rewrite some of the code and get a feel for the syntax. Work to understand each line of code. Summarize the code in your own words and try to recreate it from scratch. Apply the effective techniques shown in the code to the codebase you're currently working on.

Producing Value
---------
"If your values are sound, your writing will be sound. It all begins with intention. Figure out what you want to do and how you want to do it, and work your way with humanity and integrity to the completed article. Then you'll have something to sell" (264). Zinsser's advice here can be applied to creating software products. Work hard with intention, keep your values in place, and put in the work required to produce the product you set out to create. Money will be a side effect making your vision a reality.

Advice for Code Reviews
---------
"Clarity is what every editor owes the reader. An editor should never allow something to get into print that he doesn't understand" (292). The act of performing a code review is similar to that of an editor reviewing a publication. Both the code reviewer and editor serve as a gatekeeper for the work to be accepted. The goal of each position is to make the end product better. Allowing code into a code base that no other developer understands is a quick way to kill a project. As code reviewers we should hold each other accountable for writing code that is understandable. 


Towards Mastery
---------
There are so many other great bits from Zinsser that deserve to be shared. "If you would like to write better than everybody else," Zinsser writes, "you have to want to write better than everybody else. You must take an obsessive pride in the smallest details of your craft" (289). This advice maps directly to writing code. In order to write code well, we have to go deep into the details. Every variable, function, class, line of code needs to be reasoned out. All of these assets need to be brought together to form a cohesive solution.

The last, and maybe the strongest, message that Zinsser leaves us with applies to any skill. Zinsser wrote this passage while discussing how to deal with editors. Here you can substitute "editor" with boss, code reviewer, employers, or nobody. The points here capture the spirit of my Dev-eryday project as well as words can. Everyone who wants to be a good writer or software developer can get there. There is a path forward, you've got to be patient, be disciplined, take ownership, and believe in the process. I'll leave you with Zinsser's words, apply them to any ability you desire to improve. "Take your talent as far as you can and guard it with your life. Only you know how far that is; no editor knows. Writing well means believing in your writing and believing in yourself, taking risks, daring to be different, pushing yourself to excel. You will write only as well as you make yourself write" (293).

[oww]: https://www.amazon.com/Writing-Well-Classic-Guide-Nonfiction/dp/0060891548
[style]: https://www.amazon.com/Elements-Style-William-Strunk-Jr/dp/194564401X