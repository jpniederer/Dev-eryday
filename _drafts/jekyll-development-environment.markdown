---
layout: post
title:  "Jekyll Development Environment"
date:   
categories: jekyll
---
Setting up a development environment for Jekyll was a little bit of an experience. The docs claim that only Mac and Linux operating systems are supported, but the community has written articles on how to get the environment set up in Windows. From briefly looking at some of the steps required to run Jekyll on Windows (using the Chocolately package manager to install many packages), I decided my time would be better spent either setting pursuing another path. Going outside of Windows would not only be the cleanest approach, but also be a chance to get reaquainted to a *nix platform.

Paths Attempted
--------------
+ Setup Local Linux VM in Virtual Box

  My first choice was to setup an Ubuntu VM in Virtual Box. The idea behind this was that it'd be quick and free. So I downloaded the latest LTS version of Ubuntu (16.04) and provisioned the new VM. When I went to start it up, I got the following error message: Failed to open a session for the virtual machine Ubuntu. VT-x is not available (VERR_VMX_NO_VMX).

  After a couple of Google searches, I discovered that there were two potential causes.

  1. Virtualization is Not Turned on in System BIOS
  2. Hyper-V Needs to be Disabled so Virtual Box Can run

  I rebooted my machine to check my BIOS settings. Everything checked out, the virtualization feature was enabled. So that wasn't the solution.

  The next step was to attempt to disable Hyper-V. Through running CMD as an administrator, the command below should disable Hyper-V after rebooting the machine.

  {% highlight batchfile %}
  dism.exe /Online /Disable-Feature:Microsoft-Hyper-V
  {% endhighlight %}

  On my PC, this command was unsuccessful all three times I ran it failing to make the update after the reboot. It was time to try my next option.

+ Create a Linux VM on Azure

  Since the machine that I'd be using would only need to be used for development, there was no need to create a system with much computing power. Azure offers their smallest VM for the low price of $13.39 month, which is cheap enough to make it worth having around for learning or testing purposes. Other cloud providers may be cheaper, but Azure's offering has always delivered for me. The machine was generated with 0.75 GB of RAM and 20 GB of disk size. In practice this size has been enough since the install is super clean.

Setting up Linux for Jekyll
---------------
The bash commands below should work to setup up the Jekyll development environment on a Linux system. The commands will install needed packages and also download the (current) latest version of rubygems from the project site.

{% highlight bash %}

sudo apt-get install ruby
sudo apt-get install ruby-dev
sudo apt-get install make
sudo apt-get install g++

wget https://rubygems.org/rubygems/rubygems-2.6.8.tgzinstall rubygems
tar xvf rubygmes-2.6.8.tgzinstall
cd rubygems-2.6.8
sudo ruby setup.rb

sudo apt-get install build-essential
sudo apt-get update
sudo gem install bundler
sudo gem install jekyll

{% endhighlight %}

Once these commands have been ran, you should be able to build Jekyll projects in your environment. I received an error stating, "Error installing Jekyll, failed to build gem extension" the first time I tried to build a test project. Through reading the error messages and searching the internet a bit, I was able to identify all of the required packages and then build my test project.

Useful Jekyll Commands
--------------
In my brief time playing with environment and tools, I've found the following commands to be useful.

{% highlight bash %}

jekyll new project-name
jekyll build
jekyll serve --host=0.0.0.0

{% endhighlight %}

These commands will do the following:
  1. Generate a new Jekyll project with the name provided. It will create a new directory with some example files to help get you started.
  2. This command will build your project and create the static files that will be your website.
  3. With using an Azure VM, this is the command that I find be invaluable. This will serve the Jekyll site at servers IP address so that I can navigate to the version of the site running in the cloud from my local PC's browser. If the standard "jekyll serve" command is ran, the site will run on the localhost and only be accessible from the VM.