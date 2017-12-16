---
layout: post
title:  "Five in Five Week Two: Elixir Introduction"
date: 2017-12-8 20:45:00 +0000
categories: Challenge
---

There's no rest for the wicked. It's time for week two of my [Five Languages in Five Weeks][fnf] challenge. Week one, covering [TypeScript][ts], is the books and it's time to move on to [Elixir][ex]. My study of Elixir will take place between December 8, 2017 and Thursday, December 14, 2017. I'm planning to dive right in and write code in Elixir everyday over the next week. I should learn quite a bit.

### Why Elixir?
Elixir is a language that I've tried to learn a couple of times now. Once back in 2016 and another brief period this summer. It seems like a great language but I never used it with enough consistancy to actually learn it. The way that Elixir breaks everything out into fault-tolerant processes is a huge draw. The functional design is a big plus too. It's definitely a different flavor than I'm used to, and that's a good thing.

### Planned Projects
I've planned out a few projects that I intend to complete using Elixir. These projects are based primarily on those completed during [week one][repots] of the challenge. None of these are too large, but they will serve well as an introduction to the language. I would like to complete a decent sized project using the language but I don't know how reasonable that would be at this point. I'll just have to see how the week plays out and shift accordingly.

Here are the projects that I've planned out so far.

**[HelloElixir][hex]** - A hello world program written in Elixir.  
**[LanguageFeatures][lf]** - This project exists to demonstrate essential features of the language.  
**[RosettaCode][rc]** - Code written to compare the styles of all languages. The goal is to implement the same code accross each language.  
**[TestingElixir][tt]** - Project created to get familiar with automated testing using Elixir.  

### Repo
All of the code I write as part of the challenge will be published to GitHub. The repository is called [FiveInFive-Elixir][repo]. 

### Installation Process
Installing Elixir is extremely easy if you have [brew][brew] installed. The iex command can be used to start Elixir in interactive mode.

```
brew update
brew install elixir
iex
```

### Thoughts Coming into the Language
Since I first thought up the Five Languages in Five Weeks challenge, this was probably the week I was looking forward to the most. Elixir as a language has a ton going for it. It's functional, scalable, fault-tolerant, and trendy. It runs on the rock solid [Erlang/OTP][erl] runtime. It even has a thriving web framework, called [Phoenix][pho], that uses it to build web sites and web services. So Elixir has a ton to offer. In a perfect world I'd already be an expert with it. For now, I'm going to see how much I can learn about it this week and go from there.


[ts]: https://www.typescriptlang.org/
[repo]: https://github.com/jpniederer/FiveInFive-Elixir
[repots]: https://github.com/jpniederer/FiveInFive-TypeScript
[js]: https://developer.mozilla.org/en-US/docs/Web/JavaScript
[fnf]: https://dev-eryday.com/challenge/2017/11/30/Five-Languages-in-Five-Weeks.html
[node]: https://nodejs.org/en/
[hex]: https://github.com/jpniederer/FiveInFive-Elixir/tree/master/HelloElixir
[lf]: https://github.com/jpniederer/FiveInFive-Elixir/tree/master/LanguageFeatures
[tt]: https://github.com/jpniederer/FiveInFive-Elixir/tree/master/TestingElixir
[rc]: https://github.com/jpniederer/FiveInFive-Elixir/tree/master/RosettaCode
[re]: https://reactjs.org/
[ang]: https://angular.io/
[brew]: https://brew.sh/
[erl]: https://en.wikipedia.org/wiki/Erlang_(programming_language)