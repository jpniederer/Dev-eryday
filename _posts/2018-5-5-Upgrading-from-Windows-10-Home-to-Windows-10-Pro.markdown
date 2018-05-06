---
layout: post
title:  "Upgrading from Windows 10 Home to Windows 10 Pro"
date: 2018-5-5 20:45:00 +0000
categories: Dev-eryday
---

A few months back, I got a new Windows laptop. Even though the laptop was a fairly high end productivity machine ([Yoga 920][yg]), the device came with Windows 10 Home edition. The differences between Windows 10 Home and Windows 10 Pro aren't huge but there are some noticeable [differences][pvh]. The biggest reason for me in upgrading was that you need the Pro edition to use virtualization. With Docker becoming more of a requirement than simply a nice tool to have, it was time to upgrade from Home to Pro. Luckily, the upgrade process is simple and can be done cheaply.

Before we look at how to complete the upgrade process, let's take a look at where to buy a CD Key for Windows 10 Pro. One option is to upgrade it directly from the Microsoft Store. At the time of writing, Microsoft is charging $99 for the upgrade. The option I used was through [SCDKEY][sl] which is currently listing a Windows 10 Pro OEM key for $14. $14 is much more digestible. I recommend going through SCDKEY over upgrading through the Microsoft Store. 

Initially I was skeptical as to whether or not you could upgrade from Home to Pro using a key purchased from a third party site. Good news, it's possible and takes about five minutes total.

Right now, you can actually get a Windows 10 Pro key for $11.90 using the following code: SKTECH8. Thanks [TechBargains][tb].

![Sale Code: SKTECH8](https://farm1.staticflickr.com/966/28046539778_5d2b6fd9c8.jpg)

## Upgrade Process
1. Purchase the CD Key. I recommend going through [SCDKEY][sl] or similar. For a point of reference, SCDKEY generated my key instantly.
2. Go to Settings -> About within Windows. Click on the "Go to Store" link. The link will open up the Windows Store page for the Windows 10 Upgrade.
![Go to Store](https://farm1.staticflickr.com/971/41873460682_8b0ecec6f1.jpg)
3. On the Windows Store page for Windows 10 Pro, enter the CD Key. They should have a link that says something like, "Already have key? Enter it here."
4. Answer "Yes" to the questions about going through the upgrade process. The system will present you with a screen showing the update progress.
![Update Progress](https://farm1.staticflickr.com/975/41917339481_f8a42d0eac.jpg)
5. Let Windows restart and verify your OS Version within Settings -> About.
![Verify Windows 10 Pro](https://farm1.staticflickr.com/911/40110314430_b1c26e2802.jpg)

So that's it. It's pretty simple to upgrade from Windows 10 Home to Windows 10 Pro. It can also be quite cheap. Now it's time to get to work in Docker!

[sl]: https://www.scdkey.com/microsoft-windows-10-pro-oem-cd-key-global_1227-20.html
[tb]: https://www.techbargains.com/
[dock]: https://store.docker.com/editions/community/docker-ce-desktop-windows
[pvh]: https://gadgets.ndtv.com/laptops/features/windows-10-home-vs-windows-10-pro-differences-new-features-718532
[yg]: https://www3.lenovo.com/us/en/tablets/convertibles/yoga-900-series/Yoga-920-13/p/88YG9000859