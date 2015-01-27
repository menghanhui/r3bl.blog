---
author: Aleksandar Todorović
comments: true
date: 2014-12-15 03:56:53+00:00
layout: post
slug: facebook-hack-no4
title: 'Some Basic Facebook "Hacks" - Hack no. 4: DDoS a Website By Using Facebook'
categories:
- Cyber Security
- Projects
tags:
- projects
- Facebook
- hacking
image:
  feature: abstract-1
---

So, today I'm going to share with you a trick to DDoS a certain website by using Facebook's notes feature. The process, although pretty simple, is a bit more complicated than previous posts I wrote in this series.

So, what do you need to do?

Well, first of all, you go to the target's website and create a list with unique photos posted on that website. You put them in appropriate HTML tag like this:


<img src="http://targetname/file?r=1" />




<img src="http://targetname/file?r=2" />




...




<img src="http://targetname/file?r=1000" />






The next thing you need to do is to write a note on [m.facebook.com](http://m.facebook.com/) (it's a mobile version of Facebook).

Now, you need to duplicate that note a couple of times with one _or_ several other Facebook accounts.

After you've done that, all you need to do is to open that notes at the same time and watch the site go down. This process will generate thousands of HTTP requests in a couple of seconds to the target site.

You might want to check out previous posts in the series:




  * [Some Basic Facebook “Hacks” – Hack no. 1: Check who’s your biggest “stalker” without leaving Facebook](https://aleksandartodorovic.wordpress.com/2014/11/13/facebook-hack-no1/)


  * [Some Basic Facebook “Hacks” – Hack no. 2: Find out who’s calling you on your phone by using Facebook](https://aleksandartodorovic.wordpress.com/2014/11/13/facebook-hack-no2/)


  * [Some Basic Facebook “Hacks” – Hack no. 3: See Locked Profile Picture in Full Size](https://aleksandartodorovic.wordpress.com/2014/11/20/facebook-hack-no3/)
