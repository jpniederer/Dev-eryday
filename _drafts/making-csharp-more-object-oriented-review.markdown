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
Wrapping code in a foreach or similar loops makes code hard to reason about the purpose, difficult to prove its correctness, and makes finding bugs a challenge. For these reasons we should aspire to not use loop structures. A sequence should be able to loop through itself. In .NET languages, LINQ extension methods can be created to replace loops. LINQ versions often require less code to write and are far more readable than their loop counterpart.

Splitting Structure and Operations
-----------
The Composite Pattern is a means of building a collection of objects of the same type into a new object that implements the same interface. We can act on the composite object in the same ways we can the standard one since the same interface is used for both objects. Concrete classes need to be given meaningful names. For instance, we should prefer to present a type Painters for storing a collection of Painter objects over presenting IEnumerable<Painter> to consumers. 

Strategy Objects and Algorithms
-----------
Algorithms that vary in time can be turned into objects. By turning algorithms into objects, we can use them as interchangable pieces and call the right one based on the current circumstances. We should favor composition over inheritance, because composition is more flexible. Inheritance can be added to improve the consuming client code readability. Sometimes algorithms can be made general. We should do this when possible to avoid duplicate code and take advantage of similarity. Refactor code one step at a time in order to improve the system's design. When changes need to be made, add a class to achieve the desired result. Leave the existing classes the same, this idea follows along with the [Open Closed Principle][ocp].

Immutable Objects
-----------
Aliasing bugs can occur when shared objects are accessible in more than one location. The shared object can be modified in multiple places so the state may not be as expected. We can avoid aliasing bugs by converting entities (objects that can be mutated) into values (immutable objects). Since the value objects are immutable, their state cannot be changed simplifying code maintenance and making the system more stable. One downside of value objects is that they require more code than entities.

Special Case Objects
-----------
We can create special case objects to handle common occurances. One such special case object would be to create an object that replaces null. This technique allows us to not have to check for null references. Without having null references, all objects can be treated the same and the code is simplified.

Optional Objects
-----------
Use optional objects to handle null references when the [null object pattern][nop] and special case object aren't applicable (i.e. when no object exists). Optional objects are implemented as a collection where the collection contians one object or none. When there is an object in the collection the method is called, otherwise nothing is called. This allows us to never return null, eliminates null checking, and makes the code more readable.

Avoiding Switch Statements
-----------
Switch statements can easily become unwieldy and are not objects. Classes have to be forced into switch statement structure and modifying the switch statement forces the containing class to be updated leading to maintainability issues and potential bugs. Dynamic dispatch can be used to replace switch statements by encapsulating state in separate classes. State objects are mapped to their operations through a simple dictionary based key/value store. 

Chaining
-----------
if instructions can be converted into distinct rule objects. Once the rule objects are defined, we can order the rules by priority and process them according to their priority. The benefits of this practice is that the rules can be swapped at run time and their priorities can be updated as needed. 

Overall
-----------
This was an amazing course with a ton of ideas that need to be examined further for complete understanding. I will be working through and thinking about this material for weeks to come, and I look forward to it. This course expanded my horizons on how object oriented code should be written. Previously, I was content using a fair amount of if-else constructs. Now I'm actively trying to use good design to avoid them when it's advantageous.

After watching this course, I'm planning on doing some major refactorings to the SimpleHealthTracking code base to take advantage of some of the techniques presented in the course. Refactoring SimpleHealthTracking would also be an opportunity to reinforce the material. 

[srp]: https://en.wikipedia.org/wiki/Single_responsibility_principle
[ocp]: https://en.wikipedia.org/wiki/Open/closed_principle
[nop]: https://en.wikipedia.org/wiki/Null_Object_pattern