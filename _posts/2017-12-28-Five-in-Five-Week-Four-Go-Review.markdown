---
layout: post
title:  "Five in Five Week Four: Go Review"
date: 2017-12-28 15:20:00 +0000
categories: Challenge
---
[Go][go] wasn't really what I expected it would be. I came into the language thinking it would be a standard general purpose object oriented programming language like C# or Java, but that's not the case at all. Go is a lot closer to C than either of those two programming languages, but supports object oriented principles. That makes sense as Go was orginally created to fix some of the short comings of C. My week spent with Go showed that Go is a modern, fully featured language that has a lot going for it.

![Go Logo](https://farm5.staticflickr.com/4686/24361899717_1f0b3e62f7_z.jpg)

Go is quite a change of pace from the last two weeks featuring Elixir and Haskell. Both Elixir and Haskell are functional languages, have immutable objects, and declarative by nature. Go on the other hand is procedural, imperative, and allows for state updates on values. Moving from the functional languages to Go is a really big difference. I enjoyed the major leap.

### Procedural, Flexible, Fast
Go is flexible. It's compiled, has a garbage collector, statically typed with advanced type inference, and supports concurrent programming. You can even bend the language to use object oriented programming concepts. Go has built for support interfaces and composition which allow developers to utilize encapsulation, message passing, polymorphism, and many of the good parts of inheritance without the baggage that comes with traditional inheritance. Another major selling point of Go is that the compiled package design of Go helps make it fast. Go code typically performs well in [benchmarks][bench].

One part of the Go environment that I didn't like was the repo structure. I didn't dig too far into the specifics and can't claim to be expert on this, but the compiler will look for packages only in specific directories. When you build a package, Go will dump a copy of it to your repo and it can then be imported into your other packages as needed. I side stepped this and used "go run file.go" to run my toy programs. This environment behavior is the first thing I would research if I were to start studying Go seriously.

### Further Learning Plans
I would like to dig further into Go at some point in the future. I would say that it's my second favorite language from the challenge, behind Elixir. If I were going to learn Go, I would continue reading *[The Go Programming Language][tgp]*. I was only able to get through the first four chapters and there is a ton of wisdom to be gained for the book. Beyond that, my next step would be to implement a web service using Go.

Right now I'm not planning to learn Go in 2018 but may pick it back up at some point.

### Resources
I was able to pull from a few resources to learn Go this week.

*[The Go Programming Language][tgp]* by Alan Donovan and Brian Kernighan. This book is the best way to deeply learn Go.  
[Go Fundamentals][gof] by Nigel Poulton. Perfect course to get up to speed on the basics of Go quickly.  
[Object-Oriented Programming with Go][oogo] by Martin Van Sickle. This course shows how Go developers can take advantage of object-oriented ideas within their code. This is a very interesting course.  

### Quick Final Thoughts
Programming in Go is a very enjoyable experience. In the short time I spent with it, Go feels like a more modern C. The number of key words in the language is small and picking up the basics of the languages felt natural. I honestly think I could read through the [docker][doc] and [kubernetes][kub] source right now and get a lot out of the experience. I might not understand it all, but it would be a great learning opportunity.



[pe]: https://pragprog.com/book/elixir13/programming-elixir-1-3
[eia]: https://www.manning.com/books/elixir-in-action
[pp]: https://pragprog.com/book/phoenix/programming-phoenix
[expl]: https://app.pluralsight.com/library/courses/elixir-getting-started/table-of-contents
[ah]: https://en.wikipedia.org/wiki/Anders_Hejlsberg
[ts]: https://www.typescriptlang.org/
[repohs]: https://github.com/jpniederer/FiveInFive-Haskell
[repots]: https://github.com/jpniederer/FiveInFive-TypeScript
[repoex]: https://github.com/jpniederer/FiveInFive-Elixir
[repogo]: https://github.com/jpniederer/FiveInFive-Go
[js]: https://developer.mozilla.org/en-US/docs/Web/JavaScript
[fnf]: https://dev-eryday.com/challenge/2017/11/30/Five-Languages-in-Five-Weeks.html
[node]: https://nodejs.org/en/
[hts]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/HelloTypeScript
[lf]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/LanguageFeatures
[tt]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/TestingTypeScript
[rc]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/RosettaCode
[book]: https://basarat.gitbooks.io/typescript/
[red]: https://github.com/reactjs/redux
[er]: https://en.wikipedia.org/wiki/Erlang_(programming_language)
[px]: http://phoenixframework.org/
[hsp]: https://app.pluralsight.com/library/courses/haskell-fundamentals-part1/table-of-contents
[lgg]: http://learnyouahaskell.com/chapters
[re]: https://maciek.io/rest-api-in-haskell/
[hs]: https://www.haskell.org/
[go]: https://golang.org/
[oogo]: https://app.pluralsight.com/library/courses/go-object-oriented-programming/table-of-contents
[tgp]: https://www.amazon.com/Programming-Language-Addison-Wesley-Professional-Computing/dp/0134190440/
[gof]: https://app.pluralsight.com/library/courses/go-fundamentals/table-of-contents
[bench]: https://benchmarksgame.alioth.debian.org/u64q/measurements.php?lang=go
[kub]: https://github.com/kubernetes/kubernetes
[doc]: https://github.com/docker/docker-ce