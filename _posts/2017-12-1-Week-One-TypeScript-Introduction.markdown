---
layout: post
title:  "Week One: TypeScript Introduction"
date: 2017-12-1 10:35:00 +0000
categories: Challenge
---

Welcome to week one of my [Five Languages in Five Weeks][fnf] challenge. Week one, spanning from Friday, December 1, 2017 to Thursday, December 7, 2017, covers the [TypeScript][ts] language. I'm planning to dive right in and write code in TypeScript everyday over the next week. It's going to be a good time.

### Why TypeScript?
I choose TypeScript for the first language of the challenge because it's a language that I realistically could see myself using a lot in the future. TypeScript is a superset of [JavaScript][js] that adds static typing and various other features to the language that powers the modern web. Dynamic typing is great for writing up quick scripts and offers a ton of flexibility, but as systems grow it's nice to have the extra safety of static typing. Sometimes I've felt that I'd like JavaScript to be more like C# or Java where the compiler can pick up on bugs type based bugs before I even build my code. So TypeScript is a very natural first language choice and will allow me to ease into in the challenge. 

### Planned Projects
I've planned out a few projects that I intend to complete using TypeScript. None of these are too large, but will serve well as an introduction to the language. I would like to complete a decent sized project using the language but I don't know how reasonable that would be at this point. I'll just have to see how the week plays out and shift accordingly.

Here are the projects that I've planned out so far.

**[HelloTypeScript][hts]** - A hello world project written in TypeScript.  
**[LanguageFeatures][lf]** - This project exists to demonstrate essential features of the language.  
**[RosettaCode][rc]** - Code written to compare the styles of all languages. The same program is implemented accross each language.  
**[TestingTypeScript][tt]** - Project created to get familiar with automated testing using TypeScript.  

### Repo
All of the code I write as part of the challenge will be published to GitHub. The repository is called [FiveInFive-TypeScript][repo]. 

### Installation Process
Installing TypeScript is a pretty easy task. All you have to do is install NodeJS, which will install npm, and then issue the npm command to install TypeScript. At the time of installation, I was at version 8.9.1 for NodeJS, 5.5.1 for npm, and 2.6.2 TypeScript.

```
Install [NodeJS][node]
npm -g install typescript
```

### Thoughts Coming into the Language
Though not an essential language to learn, I feel like TypeScript adds enough benefits to JavaScript that make it worth investing time into. Sure, modern JavaScript is a great language already with the addition of ES6 and ES7 features, but its flexibility can make it opaque and tricky to reason about sometimes. Adding formal type requirements makes it easier to reason about the code you read and can prevent many common type-related errors. I feel like TypeScript is a tool that will take my JavaScript skills up a notch. Since TypeScript compiles down to JavaScript, it can be used anywhere that JavaScript is used. I think it would be beneficial to large [React][re] projects to use TypeScript over JavaScript. It definitely seems to have taken off in the [Angular][ang] world.


[ts]: https://www.typescriptlang.org/
[repo]: https://github.com/jpniederer/FiveInFive-TypeScript
[js]: https://developer.mozilla.org/en-US/docs/Web/JavaScript
[fnf]: https://dev-eryday.com/challenge/2017/11/30/Five-Languages-in-Five-Weeks.html
[node]: https://nodejs.org/en/
[hts]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/HelloTypeScript
[lf]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/LanguageFeatures
[tt]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/TestingTypeScript
[rc]: https://github.com/jpniederer/FiveInFive-TypeScript/tree/master/RosettaCode
[re]: https://reactjs.org/
[ang]: https://angular.io/