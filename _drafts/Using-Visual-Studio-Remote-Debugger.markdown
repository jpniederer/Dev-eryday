---
layout: post
title:  "Using the Visual Studio Remote Debugger"
date: 2017-4-25 22:00:00 +0000
categories: Visual Studio
---
So there I was, facing an error on a QA server that I couldn't replicate in my development environment. The only message returned from the web page was "There was an error processing your request." How in the world was I supposed to trouble shoot it? Scenarios like this seem to happen all too often. It's working in the local development environment, but not on the QA server. Luckily, Microsoft offers the [Visual Studio Remote Debugger][rd] which allows you to debug your code running outside of your local development sandbox. The software you create can be debugged both locally, running within another process on your PC, or remotely on another PC. The Visual Studio Remote Debugger is a tool that every .NET should at least be aware of.

Steps to Use the Remote Debugger
--------
These steps are written from the perspective of debugging code that has been deployed to a remote server that doesn't have Visual Studio installed.

1. Install the Remote Debugging Tool

    Ensure that the version you install corresponds with the version of Visual Studio you are using to develop the solution. Here is the [link][install] to install the 2017 version of the tools.

2. Build a Current Debug Version

3. Deploy the Debug Version to the Server

4. Run Debugging Tools as Admin on the Remote PC

5. Attach to Process Within Visual Studio

    Here you may have to sign in to an account that has admin permissions on the remote PC.

6. Set Break Points in Visual Studio

    If everything has been completed correctly, the breakpoints should show up in solid red.

7. Trigger the Break Point and Debug the Code

    Now you can step through the code and see exactly how the system is behaving. Identify the errors and get a plan together for how to resolve the problems.

Cases Where The Remote Debugger Can Be a Lifesaver
--------
1. Self Developed dll Called from a Third Party Application
2. Troubleshooting Any Deployed Executable

In the end, it turned out the error I was experiencing was very minor. The account being used to access the database on the QA server did not have access to secondary database that was being called via an insert trigger on one of our entities. Once the account was granted access to the secondary database everything worked as planned. The Remote Debugging Tool made this error trivial to find and probably saved me a great deal of time.

[rd]: https://msdn.microsoft.com/en-us/library/y7f5zaaa.aspx
[install]: https://www.visualstudio.com/downloads/#remote-tools-for-visual-studio-2017