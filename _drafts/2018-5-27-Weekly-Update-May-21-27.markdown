---
layout: post
title:  "Weekly Update: May 21 - 27, 2018"
date: 2018-5-27 11:21:00 +0000
categories: Dev-eryday
---

It's never fun when you spend a night trying to fix a small problem. I just spent almost a whole night trying to solve a problem on LeetCode called [Longest Palindromic Substring][lps]. The problem is exactly as its title suggests: given a string, find the longest substring within it that is a palindrome. For about 10 minutes I played with the idea of using a reversed version of the string to pinpoint where the longest substring was in a direct manner. This was not successful. Then it dawned on me, [dynamic programming][dp]! So, I drew out a few examples by hand and had the solution ready to code up. The solution would rest on an `int[][] lengths` that tracks the length of each candidate substring. Each time a candidate is found with a length greater than the max, it's evaluated to see whether it's a palindrome or not. If it is, we'll store the index and it's length to pull it out once we've found the solution.

That sounds like it should work, doesn't it? Well, it did, for 99 tests, but it hit a dreaded "Memory Limit Exceeded" error. I copied out the test case for the failing test and it worked in ~100ms but it was still using too much memory. So, I reworked the algorithm trying to find any places where I could free up memory. Finally, after about an hour of messing around with it, I realized that I didn't an `int[][]` a `short[][]` would be more than sufficient since the maximum possible string length was 1000. I updated the method to use a short and all was well. The code passed the tests and I knocked the problem off my todo list. 2^32 vs. 2^16 can make the difference between having enough memory or not.

![Everyday](https://farm1.staticflickr.com/967/41362483664_6321808246.jpg)



## Finished

**Pluralsight Course(s):** [Getting Started with Visual Studio Team Services (2018)][vsts]

**Book(s):** *[Code: The Hidden Language of Computer Hardware and Software][code]*

## Currents

**Pluralsight Course(s):** [React 16 - The Complete Guide][re], [Play by Play: Visual Studio Code Can Do That][vsc]

**Book(s):** *[Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation][cd]*, *[Snowcrash][snow]*

## On the Next...



[re]: https://www.udemy.com/react-the-complete-guide-incl-redux/
[cd]: https://www.amazon.com/Continuous-Delivery-Deployment-Automation-Addison-Wesley/dp/0321601912
[code]: https://www.amazon.com/Code-Language-Computer-Developer-Practices-ebook/dp/B00JDMPOK2/
[jss]: https://app.pluralsight.com/library/courses/play-by-play-javascript-security/table-of-contents
[vsts]: https://app.pluralsight.com/library/courses/getting-started-visual-studio-team-services-2018/table-of-contents
[son]: https://sonarwhal.com/
[owa]: https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project
[oid]: https://github.com/IdentityModel/oidc-client-js
[cf]: https://codefights.com/
[snow]: https://www.amazon.com/Snow-Crash-Novel-Neal-Stephenson-ebook/dp/B000FBJCJE/
[vsc]: https://app.pluralsight.com/library/courses/play-by-play-visual-studio-code-can-do-that/table-of-contents
[vscode]: https://code.visualstudio.com/
[fb]: https://firebase.google.com/
[az]: https://azure.microsoft.com/en-us/
[team]: https://www.visualstudio.com/team-services/
[auth]: https://firebase.google.com/products/auth/
[lps]: https://leetcode.com/problems/longest-palindromic-substring/description/

