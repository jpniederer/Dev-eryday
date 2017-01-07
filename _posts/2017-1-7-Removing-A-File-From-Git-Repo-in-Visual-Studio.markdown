---
layout: post
title:  "Removing a File From a Git Repo in Visual Studio"
date: 2017-1-7 16:30:00 +0000
categories: [Git, Visual Studio]
---
On more than one occasion, I've accidently committed a file to GitHub that I didn't intend to. I should have had these files in the gitignore file before checking in the code but I forgot. It's definitely a best practice, to review what's being commited before pushing the code online. Mistakes happen all the time though, so luckily there's a fix. You can use the process laid out below to remove the unwanted file from the repository when accidently checking in a file that you didn't mean to push to the repo.

Steps
-------------
1\. Update the gitignore file for the repository has an entry excluding the file that needs to be removed.
2\. Issue the command below from a git enabled shell (I used Powershell on my Windows PC):

    {% highlight batchfile %}
    git rm --cached "C:\Exact\File\Path\FileName.ext"
    {% endhighlight %}
3\. Commit the changes to the repo.

At this point the offending file will no longer be present in the Git repo. Be sure to copy it to any other PCs that will need some form of that file in the future, because it will no longer get the latest verison of the file when pulling the latest version.

Microsoft's page with the [instructions][ms-link] has the steps for this use case at the very bottom of the page. The first time I had this issue it took a while to find the explicit actions that I needed to take to resolve the problem. I'm sure I'll probably have to come back and use these steps at some point in the future. Thanks past me, you're the best.

[ms-link]: https://www.visualstudio.com/en-us/docs/git/tutorial/ignore-files