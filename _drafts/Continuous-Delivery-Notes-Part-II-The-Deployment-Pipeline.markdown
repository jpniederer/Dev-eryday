---
layout: post
title:  "Continuous Delivery Notes Part II: The Deployment Pipeline"
date: 2018-5-10 16:04:00 +0000
categories: books
---

Released in 2010, Jez Humble and Dave Farley's *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]* has become the go to resource for teaching software developers about deploying software. The book aims to teach readers best practices on how to release software as quickly and as safely as possible. The most successful technique that the authors have found is through the use of continuous delivery.

### Part II: The Deployment Pipeline

deployment pipeline - an automated manifestation of your process for getting software from version control into the hands of your users.

### Chapter 5: Anatomy of the Deployment Pipeline

Deployment is when the software goes from developer to user. Throughout the development we will have ideally went through the deployment process in the test environment many times. Versions of the software that are unfit for release, those that don't pass tests, will be marked and fixed.

Stages of the Deploymnet Pipeline:
* Commit Stage - Asserts that the system works at the technical level. It compiles, passes a suite of automated tests, and runs code analysis.
* Automated Acceptance Test Stages - Asserts that the system works at the functional and nonfunctional level, that behaviorally it meets the needs of its users and the specifications of the customer.
* Manual Test Stages - Asserts that the system is usable and fulfills its requirements, detect any defects not caught by automated tests, and verify that it provides value to its users. These stages might typically include exploratory testing environments, integration environments, and user acceptance testing.
* Release Stage - Delivers the system to users, either as packaged software or by deploying it into a production or staging environment.

Only build the binaries one time during the deployment pipeline. Build them during the commit stage and use the build throughout the entire deployment pipeline. Multiple builds is problematic because it can lead to subtle differences between the binaries. Use a single binary to minimize risk.

Deploy via the same process to each environment. Automate as many steps as possible to reduce the opportunities for mistakes along the way.

Verify each deployment.

The testing environment should be as similar to production as possible. We need as much confidence in our deployment to production as possible. By having a similar testing environment, we can iron out any issues that exist prior to moving the release to production.

If the release fails at any stage of the pipeline the build is halted and marked as a failed build.

### Chapter 6: Build and Deployment Scripting

The aim of this chapter is to introduce notable build tools and share tips and tricks around scripting out your build and deployment processes. A number of build tools are given brief overviews. Build tools covered include: Make, Ant, MSBuild, Maven, Rake.

All build scripts should be kept in version control. Build scripts are first class citizens of your project and every bit as important as the codebase.

Tips
* Always Use Relative Paths
* Eliminate Manual Steps
* Build In Traceability from Binaries to Version Control
* Don't Check Binaries into Version Control as Part of Your Build
* Test Targets Should Not Fail the Build
* Constrain Your Application with Integrated Smoke Tests

### Chapter 7: The Commit Stage

The Commit Stage is the first step in the deployment pipeline. Code is commmited and then compiled. New binaries are built, analyzed for health, and tools, such as test data and database update scripts, needed later in the pipeline are created. The commit stage should provide fast feedback so that errors are caught early. Developers need ownership of the commit stage because their work is intimately tied to the commit stage.

There are a number of practices to follow when testing at the commit stage. The tests should avoid the UI, rely on dependency injection, stay away from the database, avoid asynchrony, use test doubles, minimize state, fake times to handle all possible occurrances. 

### Chapter 8: Automated Acceptance Testing



### Chapter 9: Testing Nonfunctional Requirements



### Chapter 10: Deploying and Releasing Applications



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