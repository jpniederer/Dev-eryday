---
layout: post
title:  "Deploying Dev-eryday to GitHub Pages"
date:   
categories: jekyll
---
Deploying my Dev-eryday Jekyll project to GitHub Pages was a fairly painless process. GitHub is amazingly developer friendly and provides some truly great documentation to move the process along.

Major Steps
------------

+ Set GitHub Page for the GitHub Repository
  
  Navigate to the settings for the GitHub repository and enable the pages feature. For my project, I set it up to use the Master branch of the repo and then also set it up to use a custom domain.

+ Add A Records at DNS

  This step was the least straight forward due in large part to not being able to find adequate documentation on my DNS provider's site. Luckily, GitHub's [page][A-name] on the subject filled in enough gaps to infer the rest. Creating the two A records, one pointing to 192.30.252.153 and another to 192.30.252.154, was as easy as finding the Manage DNS menu on my provider and setting up the two A records.

+ Commit an Update

  Once you commit an update GitHub Pages will build a new version of the Jekyll project. If the project fails to build GitHub will email you. My project wasn't building at first because I didn't have my Jekyll project files at the root of the repository. Once I moved my files everything built and Dev-eryday.com was live.

Where to Next?
-------------

I'd like to spend some time styling the site to make it more unique. The Minima theme is great and will work for now, but it'd be nice to design something that really stands out from the crowd. I'll have to keep researching the Jekyll platform and let my sub-conscience work on this task. Outside of that, I'm currently working through a course on Pluralsight called, ["Making Your C# Code More Object Oriented"][oriented]. The course is presented by Zoran Horvat and I highly recommend checking it out. It presents many fine techniques to improving code quality and demonstrates compelling uses of object oriented programming.

[A-name]: https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider
[oriented]: https://app.pluralsight.com/library/courses/c-sharp-code-more-object-oriented/table-of-contents