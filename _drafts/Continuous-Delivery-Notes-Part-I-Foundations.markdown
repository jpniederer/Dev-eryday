---
layout: post
title:  "Continuous Delivery Notes Part I: Foundations"
date: 2018-5-1 16:04:00 +0000
categories: books
---

Released in 2010, Jez Humble and Dave Farley's *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]* has become the go to resource for teaching software developers about deploying software. The book aims to teach readers best practices on how to release software as quickly and as safely as possible. The most successful technique that the authors have found is through the use of continuous delivery.

Since I'm reading this book, I want to take the time to record some thorough notes, so I can come back to them later. It'd also be nice if they helped anyone else gain knowledge too. Therefore, I'm going to record my notes here at Dev-eryday through a series of posts. There will be three total posts, one covering each section from the book. This post covers Part I, Foundations. I'm also considering doing some videos on YouTube where I go over the notes covering a couple of chapters at a time. I think that would be a fun little experiment.

### Part I: Foundations

The first five chapters of the book cover some foundational pieces that make continuous delivery possible. First, we'll take a general look at exactly what the problems with delivering software are. Then we'll start digging to concepts like configuration management, continuous integration, and testing strategies.

### Chapter 1: The Problem of Delivering Software

![Chapter 1](https://farm1.staticflickr.com/976/42072218722_8d53b9bcb2.jpg)

Our goal as professional software developers is to ideas into working software as quick as possible. The aim of *Continuous Delivery* is to introduce to tactics and best practices that can enable us to not only deliver software faster, but to also make it more reliable, supportable, and maintainable.

Deployment Pipeline - a customized automated process through building, deploying, testing, and releasing your app. A deployment pipeline is the natural conclusion of continuous integration.

There are a lot of common release antipatterns. These include: deploying software manually, deploying to a staging environment only after development is complete, manual configuration management of production environments. Generally, automate what you can and deploy both early and frequently.

Benefits of continuous integration include:
* Gives All Members of the Team the Ability to do Their Job - There is a path to obtain any previous version of the software. Test and support staff can easily get any build version of the deployed software
* Limits Errors - By automating the testing process on each check in, the team knows any time a problem has been introduced into the deployment pipeline. Configuration management ensures that environments will be the same.
* Less Stress - Consistent, incremental releases lead to confidence in the current build.
* Deployment Flexibility - With all automated configuration management and deployment process, it's easy to move the app to a new server as needed. 
  
Today, containerized environments are a perfect example of how all of these concepts have been baked into the modern deployment process.

Some Best Practices for Software Delivery
* Create a Repeatable, Reliable Process for Releasing Software - Try to make releasing your software as easy as possible. If releasing code is a burden on your team, releases will be painful and infrequent.
* Automate Almost Everything - There's a theme appearing here. It's becoming clear that automation is good, manual is bad.
* Keep Everything in Version Control - The second you don't have something is the time you need it most. Version control provides an easy way store version copies of all the text-based files needed as part of your project. Take advantage of it by putting everything in to your VCS.
* If It Hurts, Do It More Frequently, and Bring the Pain Forward - By doing it more frequently you'll feel the need to improve the process. This will turn the pain point into a strength.
* Build Quality In - Be testing all throughout the development process. Encourage everyone on the team to own the testing of the system.
* Done Means Released - Software can be considered done once it has been released into production.
* Everybody Is Responsible for the Delivery Process - Having team buy in all the way around brings the importance of the delivery process to the forefront. This also brings the team together leading to more efficiency.
* Continuous Improvement - Strive for everything to get a little bit better over time. This fits in well with Dev-eryday.

Chapter 1 is a high-level overview of what's to come in the rest of the book. Key points: automate what you can, release often.

### Chapter 2: Configuration Management

![Chapter 2](https://farm1.staticflickr.com/972/40311292010_1d2381e538.jpg)

*configuration management* - the process by which all artifacts relevant to your project, and the relationships between them, are stored, retrieved, uniquely identified, and modified.

The first step towards configuration management is to use version control. Version control, sometimes referred to as source control, allows us to capture every change made to a codebase. Every change is traceable, and we can revert to any version of the file that came previously. Having an official record of each change allows for teamwork across the codebase. Any file related to the project should be stored in version control. Some popular version control systems you can use today are: [Git][git], [Team Foundation Server][tfs], [Mercurial][mer], [Subversion][svn].

Some High-Level Tips for Using Version Control Effectively
* Keep Everything in Version Control
* Check In Regularly
* Prefer Not to Branch
* Leave Meaningful Commit Messages

Build out a system for managing dependencies. If your code depends on third party libraries or components, be sure to make a copy of all related files for each version. Being able to swap versions in and out as needed is a useful option to have. Exercise caution with checking your dependencies into source control as check in size can balloon.

Application configuration should be handled the same way at every deployment level. Keeping things configurable is a good quality to strive for, but do not let the configuration flexibility kill system usability. Complex configurations are a major pain point and often lead to code that is difficult to maintain.

Your application configuration values are every bit as important as your code. That means that you should test your configurations and check them in to version control just as you would your code. The same applies to your deployment environment. There needs to be a way to verify and record any changes that are made to your system environments.

The goal of Configuration Management is to be able to recreate your production system easily from scratch, revert to a previous version of the system, and to know that deployment environments are set up in the same way.

### Chapter 3: Continuous Integration

![Chapter 3](https://farm1.staticflickr.com/906/40311291840_c3e0d0cb87.jpg)

Continuous Integration (CI) is the practice of building the entire system and running through the automated tests after each commit. This practice solves the problem of lengthy integration sprints periodically throughout the project. Rather than performing integration at some scheduled point of the project, integration is performed every step of the way. CI leads to quicker release times, less bugs, and a better sense of how the entire system is coming along.

There are three prerequisites for continuous integration. They are:
1. Version Control
2. An Automated Build
3. Agreement of the Team

There are a number of techniques that can be used in order for continuous integration to be applied smoothly.
* Check in Regularly - Frequent check ins keep the code up to date across all members of the team. If big changes are worked on in isolation, it gets tricky when the time comes to get all the pieces working together again. It's also a good practice in general to work in more digestible pieces.
* Create a Comprehensive Automated Test Suite - Unit tests, component tests, and acceptance tests all help to validate the commit hasn't broken anything. Being able to validate the code base at each commit creates confidence in the work.
* Keep the Build and Test Process Short - The time it takes to build and test the code cannot hinder development time. When CI takes take too long, it becomes a burden to follow the process and the practice will fall away. A few minutes or less is ideal. As a project grows, it may become necessary to split the build out into multiple phases.
* Managing Your Development Workspace - Developers should have a reliable development environment where they can run through the same procedures locally. A good approach to solving this is using configuration management. Quality goes up by empowering developers to perform local builds prior to saving code to source control.

Continuous Integration Best Practices
* Don't Check In on a Broken Build
* Always Run All Commit Tests Locally Before Committing, or Get Your CI Server to Do It for You
* Wait for Commit Test to Pass Before Moving On
* Never Go Home on a Broken Build
* Always Be Prepared to Revert to the Previous Revision
* Time-Box Fixing Before Reverting
* Don't Comment Out Failing Tests
* Take Responsibility for All Breakages That Result from Your Changes
* Test-Driven Development

Popular Continuous Integration Software

### Chapter 4: Implementing a Testing Strategy

![Chapter 4](https://farm1.staticflickr.com/906/42072218652_8aa0d4197a.jpg)

A thorough, up-to-date test library is a boon to any software project. Tests bring confidence through demonstrable proof that the system works as expected, they document expected behavior, and lead to better coding practices due to the patterns required to make code testable.

Types of Tests
* Business-Facing Tests That Support the Development Process - These tests are often called functional or acceptance tests. These are the tests that validate that development has implemented the specified functionality. Functional tests are used to denote what's "done." Aim to automate these tests.
* Technology-Facing Tests That Support the Development Process - (Unit, Integration, System Tests) Tests that are built by the developers for the developers.
* Business-Facing Tests That Critique the Project - Tests that put the product in the hands of the users. Users run through the system and evaluate if the software meets their needs.
* Technology-Facing Tests That Critique the Project - These tests focus on things like system load and environment security. Considerable resources are usually needed to set these tests up.

Stay tuned for part 2, The Deployment Pipeline.

[cd]: https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912
[git]: https://git-scm.com/
[tfs]: https://www.visualstudio.com/tfs/
[mer]: https://www.mercurial-scm.org/
[svn]: https://subversion.apache.org/