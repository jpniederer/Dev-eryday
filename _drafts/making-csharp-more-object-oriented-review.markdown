---
layout: post
title:  "Course Review: Making Your C# Code More Object Oriented"
date:   
categories: Object Oriented Programming
---
I'm an unabashed fan of the Pluralsight training website. Not only does it have great learning material, but it also has an unrivaled selection of content. In the realm of training, it's like if Netflix combined with Prime and HBO Go to form one super video streaming site. Pluralsight is a fantastic resource. Lately, I've been watching the course, "Making Your C# Code More Object Oriented." It's an amazing course, one that I recommend highly. Here is a brief summary of what it covers.

Attaining Extensibility
-----------
Object oriented code allows us to write code that is extensible. A lot of code written today, even that written in fully object oriented languages like C# and Java, takes no advantage of the key features of object orientation. You can write object oriented code in any language; all code doesn't need to look like structured code written in C. Define objects to perform operations and take advantage of dynamic dispatch to handle objects that behave differently. We can improve the design of our software and have a better change of it working in the real world through using OOP.

No More Logical Branching
-----------
Poorly designed classes do everything on their own. These classes are not designed to adhere to the [Single Responsibility Principle][srp]. When classes are designed in this manner, they often have many if-then-else constructs littered throughout the class definition. This is because the single class has too many responsibilities. One potential solution to this problem is to create sparate classes to implement each possible state. The state object is substituted in the implementation to handle the case. The state pattern allows the classes we create to be simple and delegates the behavior to concrete state classes.

Sequences
-----------

Splitting Structure and Operations
-----------

Strategy Objects and Algorithms
-----------

Immutable Objects
-----------

Special Case Objects
-----------

Optional Objects
-----------

Avoiding Switch Statements
-----------

Chaining
-----------

Overall
-----------
This was an amazing course with a ton of ideas that need to be examined further for complete understanding. I will be working through and thinking about this material for weeks to come, and I look forward to it. This course expanded my horizons on how object oriented code should be written. Previously, I was content using a fair amount of if-else constructs. Now I'm actively trying to use good design to avoid them when it's advantageous.

After watching this course, I'm planning on doing some major refactorings to the SimpleHealthTracking code base to take advantage of some of the techniques presented in the course. Refactoring SimpleHealthTracking would also be an opportunity to reinforce the material. 

[srp]: https://en.wikipedia.org/wiki/Single_responsibility_principle