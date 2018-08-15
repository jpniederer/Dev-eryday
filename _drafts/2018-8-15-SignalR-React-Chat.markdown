---
layout: post
title:  "Building a Chat App with ASP.NET Core, SignalR, React, and Redux"
date: 2018-8-15 15:33:00 +0000
categories: Creations
description: In efforts to learn, I built a basic chat room application using ASP.NET Core, SignalR, React, and Redux. This is how I built it.
---

A few weeks back I set out to create a Chat App using [ASP.NET Core SignalR][snr]. It all started when I worked through Roland Guijt's [Getting Started with ASP.NET Core SignalR][pssnr] on Pluralsight. The course was brief, but it made it evident that SignalR would be a perfect technology for building a chat room type app. Guijt demonstrated the power of SignalR through building a coffee ordering system that automatically notified customers of the process of making their drink. That app was great, but it was time for more information from the source, so I headed to Microsoft's official [docs][sic]. SignalR is so well suited for a chat app that Microsoft's official ["Getting Started" tutorial][gst] for the technology is to build a simple messaging system. With that sign of assurance, I decided to build out a simple chat app with SignalR.

After deciding to build the chat app, it was time to layout a rough design. So I got out the iPad, opened up [autodesk SketchBook][asb], and drew up a basic chat room interface. The end result was the image you see below. It's not perfect, but it conveys exactly what I wanted out of the app. 

![ReactChat Mockup](https://farm2.staticflickr.com/1810/43120206951_7b49069f66.jpg)

Right around the time that image was made, I decided that I would use [React][re] to make the frontend. Hence the name, "React Chat" featured prominently in the upper body of the image. So it was settled, I would be marrying two of my favorite technologies to come about in the last few years, .NET Core and React. While I was diving back in to React, it felt like a good time to use [Redux][rex] again. Therefore, Redux is used for state management on the frontend.

I hope that little narrative helps set the stage. What follows will give some light detail on how I built a chat application using ASP.NET Core, SignalR, React, and Redux. The application is pretty basic, but it combines a lot cool technologies. The same techniques used to build this chat app can be used to create some truly novel systems. Bringing these technologies together to create a cohesive system may seem like a challenge before you get started, I know it did for me initially, but it's suprisingly straightforward and fun once you get into it.

![Early Release of the App](https://farm1.staticflickr.com/859/42971150405_27aa94fc14.jpg)

### Backend

Before we go any further, this won't be an in depth, line-by-line walk through. I'm going to give a high level descriptions of the major steps that were taken to produce the application. This instruction should be enough to dig further into the source or potentially a hint as where to go next. If you want a great tutorial that is brief but definitely more thorough, check out *[The Little ASP.NET Core Book][lc]* by Nate Barbettini. It's the perfect primer for ASP.NET Core apps and it was the primary resource used in building out the backend.

**High Level Backend Steps**
1. Create ASP.NET Core Web Project
2. Make Message and ChatRoom Models
3. Setup DBContext and SQLite
4. Build Out Dependency Injection
5. Integrate SignalR Hubs

### Frontend


### Deployment


### Notable Links
If you've read this far, thank you! You made it through the bulk of the work. Now for some annotated links. Many of these are included in the body of the article but are included here for futher details. Each of these pages/sites played a role in the app.

  [SignalR React Chat][src] - This is the live version of the site.

  [NETCorePlayground][gh] - The repo that houses the app. My intention is to add more small, open-source ASP.NET Core apps here and use the code for write ups like this one.

  [SignalR React Chat Source][caf] - Folder from the NETCorePlayground repo containing the source code for the app. This link saves a click from the link directly above.

  *[The Little ASP.NET Core Book][lc]* - A great introduction to ASP.NET Core by Nate Barbettini. The book walks readers through building out a Todo app using ASP.NET Core.

### What's Next
I don't think I'll be spending much more time with this chat app, but there are a number of features that could be added to make it a far better application. I may add a few of them for the exercise of adding them or for the chance to write a tutorial for this site. Sometimes it just fun to add features to a little side project.

What are some features you'd add app? Feel free to fork the [repo][gh] and post your code online if you do. Note that the ChatApp is in the [ChatApp Folder][caf] within the NETCorePlayground repo. I won't hesitate to merge the code into the main branch if it fits in with the application.


[src]: https://chatappwithsignalr.azurewebsites.net/index.html
[snr]: https://www.asp.net/signalr
[gst]: https://docs.microsoft.com/en-us/aspnet/core/tutorials/signalr?view=aspnetcore-2.1&tabs=visual-studio
[sic]: https://docs.microsoft.com/en-us/aspnet/core/signalr/introduction?view=aspnetcore-2.1
[pssnr]: https://app.pluralsight.com/library/courses/aspdotnet-core-signalr-getting-started/table-of-contents
[re]: https://reactjs.org/
[gh]: https://github.com/jpniederer/NETCorePlayground
[caf]: https://github.com/jpniederer/NETCorePlayground/tree/master/ChatApp
[asb]: https://sketchbook.com/
[lc]: https://www.recaffeinate.co/book/
[rex]: https://redux.js.org/