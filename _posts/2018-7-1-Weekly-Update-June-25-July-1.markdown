---
layout: post
title:  "Weekly Update: June 25 - July 1, 2018"
date: 2018-7-1 16:00:00 +0000
categories: Dev-eryday
---

In all my time working with .NET, I've never played with the [SignalR][snr] or [ASP.NET Core SignalR][src]. That all changed this week when I worked through [Getting Started with ASP.NET Core SignalR][sig]. The course provides a very basic look into how SignalR can be used to bring real-time functionality to your projects. Clients can connect to the server via transports, typically through [WebSockets][ws], and then communicate through the hub, the name of the connection between the client and the server. The demo app created in the course features an online storefront where users can order coffee and then get real-time status updates as their beverage is prepared. I'm itching to use the course as a launching point to create a basic chatroom. Once the basic chatroom is created it could be improved with React. That could be a fun tutorial series.

![ReactChat Mockup](https://farm2.staticflickr.com/1810/43120206951_7b49069f66.jpg)

On top of the SignalR stuff, I consumed a course covering [xUnit][xu]. The course is called [Testing .NET Core Code with xUnit.net: Getting Started][xuc]. Up to this point as a .NET developer, I've used [MSTest][mst]. It's been a solid test runner and testing framework, but the popularity of xUnit makes it a tool worth exploring. For anyone else in the same boat I have good news. The transition from MSTest to xUnit is natural. Both tools are capable testing frameworks that can be used to write robust unit tests for any .NET project. When it comes to unit tests it doesn't really matter which flavor of tests you're writing, but that you're writing tests. The best testing framework is the one that you'll use.

## Finished

**Pluralsight Course(s):** [Getting Started with ASP.NET Core SignalR][sig]

**Book(s):** *[How Not to Die: Discover the Foods Scientifically Proven to Prevent and Reverse Disease][hnd]*

## Currents

**Pluralsight Course(s):** [React 16 - The Complete Guide][re]

**Book(s):** *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]*

## On the Next...

I'm looking forward to spending time working to create a chatroom app with SignalR and React. I've created a GitHub project, [NETCorePlayground][ncp], where I will be storing projects used to learn and share ideas about .NET Core development. The first project I'm tackling is "ReactChat." The picture for this week is a quick mockup that I drew. That's the target. I'm sure it'll evolve as the project comes together. I'll get a live version online as soon as I have the basic functionality in place.

[re]: https://www.udemy.com/react-the-complete-guide-incl-redux/
[cd]: https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912
[dok]: https://app.pluralsight.com/library/courses/docker-deep-dive-update/table-of-contents
[doom]: https://www.amazon.com/Masters-Doom-Created-Transformed-Culture-ebook/dp/B000FBFNL0/
[jc]: https://en.wikipedia.org/wiki/John_Carmack
[jr]: https://en.wikipedia.org/wiki/John_Romero
[api]: https://app.pluralsight.com/library/courses/play-by-play-creating-apis-developers-identity-server-four/table-of-contents
[fcc]: https://www.freecodecamp.org/
[sig]: https://app.pluralsight.com/library/courses/aspdotnet-core-signalr-getting-started/table-of-contents
[hnd]: https://www.amazon.com/How-Not-Die-Discover-Scientifically-ebook/dp/B00Y7USB14/
[snr]: https://www.asp.net/signalr
[src]: https://docs.microsoft.com/en-us/aspnet/core/signalr/introduction?view=aspnetcore-2.1
[xu]: https://xunit.github.io/
[mst]: https://docs.microsoft.com/en-us/dotnet/core/testing/unit-testing-with-mstest
[ncp]: https://github.com/jpniederer/NETCorePlayground
[xuc]: https://app.pluralsight.com/library/courses/dotnet-core-testing-code-xunit-dotnet-getting-started/table-of-contents