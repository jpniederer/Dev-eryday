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
  a

Setting up Linux for Jekyll
---------------
The bash commands below should work to setup up the Jekyll development environment on a Linux system.

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

These commands will install Ruby and the packages it requires to build Jekyll projects. I received an error stating, "Error installing Jekyll, failed to build gem extension" until I had all of these tools setup and installed.

Useful Jekyll commands
--------------
