---
layout: post
title:  "Five in Five Week Three: Haskell Introduction"
date: 2017-12-15 21:35:00 +0000
categories: Challenge
---

Another week, another language. We're already into week three of my [Five Languages in Five Weeks][fnf] challenge. Both week one and week two, covering [TypeScript][ts] and [Elixir][ex] respectively, are in the books and it's time to move on to [Haskell][hs]. My study of Haskell will take place between December 15, 2017 and Thursday, December 21, 2017. I'm going to dive right in and write code in Haskell everyday over the next week. I will learn quite a bit this week.

![Haskell Logo](https://farm5.staticflickr.com/4686/38371368494_03c28873bd_z.jpg)

### Why Haskell?
If Elixir was different from the languages I typically use, Haskell is on another planet. I've been curious about Haskell ever since I heard about it. Haskell is declarative, statically typed, and purely functional. It supports concurrency. One of the main draws to the language for me is that it's based on [lambda calculus][lc]. Haskell's firmly rooted in mathematics and I've read several testimonials that claim writing Haskell code is a lot like doing actual mathematics. 

### Planned Projects
I've planned out a few projects that I intend to complete using Haskell. These projects are based primarily on those completed during [week one using TypeScript][repots] and [week two using Elixir][repoex]. None of these projects are too large, but they will serve well as an introduction to the language. I would like to complete a decent sized project using the language but I don't know how reasonable that would be at this point. I'll just have to see how the week plays out and shift accordingly.

Here are the projects that I've planned out so far.

**[HelloHaskell][hh]** - A hello world program written in Haskell.  
**[LanguageFeatures][lf]** - This project exists to demonstrate essential features of the language.  
**[RosettaCode][rc]** - Code written to compare the styles of all languages. The goal is to implement the same code accross each language.  
**[TestingHaskell][tt]** - Project created to get familiar with automated testing using Haskell.  

### Repo
All of the code I write as part of the challenge will be published to GitHub. The repository is called [FiveInFive-Haskell][repo]. 

### Installation Process
Installing Haskell is extremely easy if you have [brew][brew] installed. brew has been the MVP of this Five in Five project so far. If you don't have brew or are on a different platform, you can use these [instructions][int] found on the Haskell site. The "gchi" command opens up a Haskell prompt.

```
brew update
brew cask install haskell-platform
gchi
```

### Thoughts Coming into the Language
Haskell is the language out of the five I'm attempting to learn (TypeScript, Elixir, Haskell, Go, and Swift) that intimidates me the most. It and Elixir are similar in terms of what each can do, but they have far different syntaxes. I'll be content if I'm able to learn some of the basics and at least write a "Hello World" program by the end of the week. I'm planning to use *[Learn You a Haskell for Great Good!][hgg]* to pick up the language basics. It seems to be a well regarded text and I've seen it recommended on [HackerNews][hn] a ton of times. It's time I found out what all the fuss about Haskell is all about. 


[ts]: https://www.typescriptlang.org/
[hs]: https://www.haskell.org/
[repoex]: https://github.com/jpniederer/FiveInFive-Elixir
[repots]: https://github.com/jpniederer/FiveInFive-TypeScript
[repo]: https://github.com/jpniederer/FiveInFive-Haskell
[js]: https://developer.mozilla.org/en-US/docs/Web/JavaScript
[fnf]: https://dev-eryday.com/challenge/2017/11/30/Five-Languages-in-Five-Weeks.html
[node]: https://nodejs.org/en/
[hh]: https://github.com/jpniederer/FiveInFive-Haskell/tree/master/HelloHaskell
[lf]: https://github.com/jpniederer/FiveInFive-Haskell/tree/master/LanguageFeatures
[tt]: https://github.com/jpniederer/FiveInFive-Haskell/tree/master/TestingHaskell
[rc]: https://github.com/jpniederer/FiveInFive-Haskell/tree/master/RosettaCode
[re]: https://reactjs.org/
[ang]: https://angular.io/
[brew]: https://brew.sh/
[erl]: https://en.wikipedia.org/wiki/Erlang_(programming_language)
[lc]: https://en.wikipedia.org/wiki/Lambda_calculus
[int]: https://www.haskell.org/platform/
[hgg]: http://learnyouahaskell.com/
[hn]: https://news.ycombinator.com/