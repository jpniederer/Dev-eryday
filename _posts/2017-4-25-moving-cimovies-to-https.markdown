---
layout: post
title:  "Moving CentralIllinoisMovies.info to HTTPS"
date: 2017-4-25 22:00:00 +0000
categories: Security
---

Back in the winter of 2014, I made a website called centralillinoismovies.info. It was pretty much a basic movie blog. It was developed in ASP.NET MVC and the site hasn't been updated for a really long time. The goal was to create as much content as possible and get a little bit of advertisement money. Well, it's been over three years since the site went live and I've got $3.00 from the ads. There was just not much demand for the site and I wasn't willing to put in the effort required to create the content that it would take to make the site a success. So I got to thinking, "What could I do to make this site worth keeping around?" Getting back into content generation isn't the answer. Using it as an opportunity to do a major refactoring exercise could be an option but there are better ways to do that. Then it hit me, I should use it as a test to make the site HTTPS compliant.

Lately I completed watching the a Pluralsight course, [Things Every Developer Must Know About HTTPS][https], by Troy Hunt. The course talks about the many benefits of HTTPS and how to update your sites to support HTTPS. If you have a Pluralsight account and any interest web development and security, I recommend watching it. Troy covers many reasons why you should make your support HTTPS and how to best go about it. Before taking the course, I always thought that it was essential to buy a certificate and continue paying for it thereafter. This assumption couldn't have been further from reality! In today's world it's not only free to get HTTPS, it's also amazingly easy.

Options
----
As with anything in the tech world, there are a number of choices to choose from. I was looking for a free cert provider since the centralillinoismovies.info site probably isn't ever going to make the investment back. The free caveat pretty much trims the available solutions down to two. Those options are:

1. [Let's Encrypt][le]

    Let's Encrypt is a free certificate provider that is really changing the game for the better. If you have lots of control over your server, this is the most flexible way to get your site certified with TLS. For my purposes, Let's Encrypt isn't the best option. My site is hosted in a shared environment on Azure's Web Services platform with no root access to the underlying OS. Azure's shared host would be incompatible with Let's Encrypt. I considered spinning up a new virtual machine to handle to host the site before hearing about option two.

2. [Cloudflare][cf]

    Cloudflare is a service platform that can be used to provide a free certificate. Cloudflare provides many other tools like caching, threat analysis, and analytics. This is the option I decided to go with in the end. The best part about Cloudflare is how remarkably easy it is to setup. Another advantage is that this solution doesn't require full control of the server.

Steps to Setup Cloudflare
----
This could not have been easier. Here are the steps that I used to get the site using HTTPS.

1. Create a Cloudflare Account
2. Enter Your Domain Name
3. Verify Imported DNS Settings with Those From Your Registrar
4. Update nameserver Records on Registrar
5. Wait for Changes to Take Effect

Cloudflare says that it can take up to 24 hours for the changes to take effect. All of the changes for centralillinoismovies.info were completed in under 30 minutes. The site never went down and is currently being served via HTTPS.

One additional thing that I did was to setup a Page Rule for the site to always use HTTPS. With the page rule enabled, Cloudflare will redirect all traffic through HTTPS. This is handy for forcing the traffic through HTTPS.

Notable Benefits of HTTPS
----
The benefits of HTTPS are overwhelming. There doesn't appear to be many, if any, compelling reasons to stick to http.
1. More Secure
2. Better SEO
3. Uses Latest Technologies (HTTP2, Brotli Compression)
4. Faster

Overall, I'm glad that I decided to move centralillinoismovies.info over to HTTPS. It's probably not going to impact the site's popularity in any way, but it did open my eyes to just how easy it is to get HTTPS on a site. In fact, after setting up HTTPS on centralillinoismovies.info, I setup up dev-eryday.com to support HTTPS too! With all of the potential benefits, and the fact that search engines are moving towards ranking HTTPS sites higher than HTTP ones, it's a no brainer to move any site you can to HTTPS.

[https]: https://app.pluralsight.com/library/courses/https-every-developer-must-know/table-of-contents
[le]: https://letsencrypt.org
[cf]: https://www.cloudflare.com