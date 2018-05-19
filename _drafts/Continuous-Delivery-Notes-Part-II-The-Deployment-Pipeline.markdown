---
layout: post
title:  "Continuous Delivery Notes Part II: The Deployment Pipeline"
date: 2018-5-10 16:04:00 +0000
categories: books
---

Released in 2010, Jez Humble and Dave Farley's *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]* has become the go to resource for teaching software developers about deploying software. The book aims to teach readers best practices on how to release software as quickly and as safely as possible. The most successful technique that the authors have found is through the use of continuous delivery.

Part II: The Deployment Pipeline

Chapter 5: Anatomy of the Deployment Pipeline

Chapter 6: Build and Deployment Scripting

Chapter 7: The Commit Stage

Chapter 8: Automated Acceptance Testing

Chapter 9: Testing Nonfunctional Requirements

Chapter 10: Deploying and Releasing Applications

### Related Resources Worth Checking Out
* *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]* - The book these notes are based on.
* [Getting Started with Visual Studio Team Services (2018)][vsts] - This is a course on Pluralsight that shows how to use Microsoft's Visual Studio Team Services. It includes sections that show how to get your project in source control, implement continuous integration, run automated tests, and setup automatic deployments.
* [Visual Studio Team Services][vs] - The actual site for Microsoft's cloud-based devops solution.
* [GitHub][gh] - The most popular online Git solution.
* [Travis-CI][tr] - This is an online continuous integration solution that integrates nicely with GitHub.
* [Docker][do] - Container solution. Containers can make the process of continuous delivery a lot smoother.
*[Working Effectively with Legacy Code][lc]* - This is a great book that talks about how to work with legacy code. A major portion of the book shares tips on how to make legacy codebases testable.

Stay tuned for part III, The Delivery Ecosystem.

[cd]: https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912
[git]: https://git-scm.com/
[tfs]: https://www.visualstudio.com/tfs/
[mer]: https://www.mercurial-scm.org/
[svn]: https://subversion.apache.org/
[vsts]: https://app.pluralsight.com/library/courses/getting-started-visual-studio-team-services-2018/table-of-contents
[vs]: https://www.visualstudio.com/team-services/
[gh]: https://github.com/
[tr]: https://travis-ci.org/
[do]: https://www.docker.com/
[lc]: https://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052/