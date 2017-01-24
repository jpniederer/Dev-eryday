---
layout: post
title:  "Building a JavaScript Development Environment Course Review"
date: 
categories: JavaScript
---

For the last week I've been taking the course, ["Building a JavaScript Development Environment"][bjde], on PluralSight. The course is led by Cory House and covers how to build a modern JavaScript development environment using many of the most popular and powerful tools available to web developers today. The course is a perfect survey of how to approach JavaScript development right now. The rational behind which tools are used is presented in a clear, and thorough manner. Alternative options are cited showing just how many choices exist in JavaScript-land. With the pace at which JavaScript moves, I'm sure some of these tools will be replaced with better options at some point in the near future, but this material is perfect for anyone wanting to kickstart their JavaScript development knowledge.

The key focus of the course is to create a robust development environment that utilizes the best tools available to developers. Through leveraging these tools, software developers and their teams can improve the quality of their code and the deliverables being created. Teams should get together and develop consistant standards for their JavaScript starting kit. 

Since JavaScript is so popular and versatile, there are lots of ways to do pretty much anything. Take transpiling, the process of writing code in another language and compiling that code to JavaScript, for instance. Here's a [list][transpilers] of transpilers we have to choose from. That's an impressive, and lengthy, list! Transpiling might be more extreme than many of the other choices we have to make, but similar problems exist for choosing our text editor, package manager, testing library, bundling and linting solutions.

My favorite section of the course was the session on HTTP calls. In that module, we built a mock HTTP library using a mock API data schema and served the mock data with JSON Server.

A potential improvement to the course would have been to flesh out the example project a little further. Implementation wasn't the focus of the course though so I'm more than happy to build the sample project out further myself.

As a developer who has primarily built projects for the web using MVC frameworks, the JavaScript development is a complex beast. There are so many decisions to be made when rolling your own project template.

[bjde]: https://app.pluralsight.com/library/courses/javascript-development-environment/table-of-contents
[transpilers]: https://github.com/jashkenas/coffeescript/wiki/list-of-languages-that-compile-to-js