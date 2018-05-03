---
layout: post
title:  "Continuous Delivery Notes Part I: Foundations"
date: 2018-5-1 16:04:00 +0000
categories: books
---

Released in 2010, Jez Humble and Dave Farley's *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]* has become the go to resource for teaching software developers about deploying software. The book aims to teach readers best practices on how to release software as quickly and as safely as possible. The most successful technique that the authors have found is through the use of continuous delivery.

Since I'm reading this book, I want to take the time to record some thorough notes so I can come back to them later. It'd also be nice if they helped anyone else gain knowledge too. Therefore, I'm going to record my notes here at Dev-eryday through a series of posts. There will be three total posts, one covering each section from the book. This post covers Part I, Foundations. I'm also considering doing some videos on YouTube where I go over the notes covering a couple of chapters at a time. I think that would be a fun little experiment.

Part I: Foundations

Chapter 1: The Problem of Delivering Software

Our goal as professional software developers is to ideas into working software as quick as possible. The aim of *Continuous Delivery* is to introduce to tactics and best practices that can enable us to not only deliver software faster, but to also make it more reliable, supportable, and maintainable.

Deployment Pipeline - a customized automated process through building, deploying, testing, and releasing your app. A deployment pipeline is the natural conclusion of continuous integration.

There are a lot of common release antipatterns. These include: deploying software manually, deploying to a staging environment only after development is complete, manual configuration management of production environments. Generally, automate what you can and deploy both early and frequently.

Benefits of continuous integration include:
* Gives All Members of the Team the Ability to do Their Job - There is a path to obtain any previous version of the software. Test and support staff can easily get any build version of the deployed software
* Limits Errors - By automating the testing process on each check in, the team knows any time a problem has been introduced into the deployment pipeline. Configuration management ensures that environments will be the same.
* Less Stress - Consistant, incremental releases lead to confidence in the current build.
* Deployment Flexibility - With all automated configuration managment and deployment process, it's easy to move the app to a new server as needed. 
  
Today, containerized environments are a perfect example of how all of these concepts have been baked inton the modern deployment process.

Some Best Practices for Software Delivery
* Create a Repeatable, Reliable Process for Releasing Software - Try to make releasing your software as easy as possible. If releasing code is a burden on your team, releases will be painful and infrequent.
* Automate Almost Everything - There's a theme appearing here. It's becoming clear that automation is good, manual is bad.
* Keep Everything in Version Control - The second you don't have something is the time you need it most. Version control provides an easy way store version copies of all the text based files needed as part of your project. Take advantage of it by putting everything in to your VCS.
* If It Hurts, Do It More Frequently, and Bring the Pain Forward - By doing it more frequently you'll feel the need to improve the process. This will turn the painpoint into a strength.
* Build Quality In - Be testing all throughout the development process. Encourage everyone on the team to own the testing of the system.
* Done Means Released - Software can be considered done once it has been released into production.
* Everybody Is Responsible for the Delivery Process - Having team buy in all the way around brings the importance of the delivery process to the forefront. This also brings the team together leading to more efficiency.
* Continuous Improvement - Strive for everything to get a little bit better over time. This fits in well with Dev-eryday.

Chapter 1 is a high level overview of what's to come in the rest of the book. Key points: automate what you can, release often.

Chapter 2: Configuration Management

Chapter 3: Continuous Integration

Chapter 4: Implementing a Testing Strategy

Stay tuned for part 2, The Deployment Pipeline.

[cd]: https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912