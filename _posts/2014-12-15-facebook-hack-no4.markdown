---
author: Aleksandar Todorović
comments: false
date: 2014-12-15 03:56:53+00:00
layout: post
slug: facebook-hack-no4
title: 'Basic Facebook Hacks - Lets DDoS a website!'
categories: en
tags:
- projects
- Facebook
- hacking
image:
  feature: abstract-1-3
---

So, today I'm going to share with you a trick to DDoS a certain website by using Facebook's notes feature. The process, although pretty simple, is a bit more complicated than previous posts I wrote in this series.

**Note:** You'll might need to use a couple of Facebook accounts.

## So, what do you need to do?

Well, first of all, you go to the target's website and create a list with unique photos posted on that website. You put them in appropriate HTML tag like this:

```
<img src="http://targeturl.example/file1.jpg" />
<img src="http://targeturl.example/file2.jpg" />
...
<img src="http://targeturl.example/file1000.jpg" />

```

The next thing you need to do is to copy this list in a note using `http://m.facebook.com/` (it's important to use the mobile version of Facebook).

After you've done that, all you need to do is to open that note from different Facebook accounts at the same time, sit back, relax, and watch the site go down. This process will generate thousands of HTTP requests in a couple of seconds to the target site.

You might want to check out previous posts in the series:

* [Hack no.1: Check who's your biggest "stalker" without leaving Facebook](https://r3bl.github.io/en/facebook-hack-no1/)
* [Hack no.2: Find out who's calling you on your phone by using Facebook](https://r3bl.github.io/en/facebook-hack-no2/)
* [Hack no.3: See locked profile picture in full size](https://r3bl.github.io/en/facebook-hack-no3/)
* [Hack no.5: Find out the location of your friends at the time they were texting you](https://r3bl.github.io/en/facebook-hack-no5)
