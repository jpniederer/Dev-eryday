---
layout: post
title:  "Installing Visual Studio from the Command Line"
date: 2017-1-19 8:00:00 +0000
categories: Visual Studio
---
After using Visual Studio daily for over five years, it's nice to still be able to learn new tricks to use it better. It's a rich, expansive development environment that can do almost anything. While troubleshooting a installation problem with the latest production version of VS (VS 2015: Update 3), I found the installation instructions on [MSDN][msd]. At the very bottom of the page, in the "Related Topics" section, there's a link that says, "Use Command-Line Parameters to Install Visual Studio." That link will take you to this [page][command] discussing the available options for installing VS from the command line. You can also use the command line instruction to repair, modify, and uninstall instances of Visual Studio.

There are a ton of customizable options that aren't available, or aren't transparent to set, when installing the product from the standard menu. Here's a summary of a few of the commands I found useful while attempting to get my local installation perfect.

| Switch  | Action  |
|---|---|
| /CustomInstallPath | Installs the packages from the specified directory. Useful if you want some packages from one version of VS and other packages from another. |
| /ForceRestart | Forces a restart upon completion of the install. |
| /full | Performs a full installation of the program.  |
| /Log *filename*  | Tells VS where to log the installation details.  |
| /NoCacheOnlyMode | Stops population of the package cache. |
| /NoRefresh| Forces the installer to not check for updates. |
| /NoRestart | Prevents the computer from restarting on completion of the install. |
| /noweb | Forces the install to not use the internet. |
| /PromptRestart | Prompts the user for restart after completion. |
| /quiet | Makes the installation run without the user interface. |
| /passive | Displays the progress of the install but no user interaction is required. |
| /repair | Switch to enter the repair of a previous VS installation. |
| /Uninstall | Uninstalls the program. |
| /force | In combination with the /Uninstall command, will force the uninstallation of VS and all related components. |

So, from the folder containing the vs_enterprise.exe file and the rest of the ISO's contents, I can issue the command below to install Visual Studio from a local folder:

{% highlight batchfile %}
    vs_enterprise.exe /full /NoRefresh /passive /noweb /log PassiveInstallLog.txt
{% endhighlight %}

This command will install VS and all related packages due to the /full switch. It won't go out to the web (/noweb) and it won't check for updates (/norefresh). The process will also run on its own due to the /passive flag. 

Installing VS from the command line is a slick feature. I'm definitely going to have to take advantage of it now that I know about it. There are lots of customization options and allows for installs, repairs, and uninstalls. Another potential use is that can easily install VS across many PCs with minimal effort through the use of the /passive and /ForceRestart switches. 

[msd]: https://msdn.microsoft.com/en-us/library/e2h7fzkw.aspx
[command]: https://msdn.microsoft.com/en-us/library/mt720584.aspx