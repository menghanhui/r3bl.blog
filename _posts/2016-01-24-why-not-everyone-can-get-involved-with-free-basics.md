---
author: Aleksandar Todorović
comments: false
date: 2016-1-24 17:27:00+01:00
layout: post
slug: why-not-everyone-can-get-involved-with-free-basics
title: 'Why "everyone can submit his website to Free Basics" is an exaggeration'
categories: en
tags:
- Facebook
- net neutrality
- Free Basics
---

With every critic of Facebook's Free Basics program, it doesn't usually take long until Facebook responds with "Everyone can submit their website to our Free Basics program". While this is technically true, and indeed, everyone _can_ submit their website to Facebook, but that does not mean that the submission will be received nor that you will receive any feedback what so ever.

During the Indian rebellion against Facebook's Free Basics that escalated about a month ago, I have decided to submit my website to Free Basics, just to see how it goes. So, on December 28th, I did just that.

I have submitted my personal website (`r3bl.me`) through [this link](https://partners.facebook.com/fbs/onboarding/). I took a bunch of screenshots during the process. Now, I will share with you how complicated the process was.

## First step: entering your personal info and info about the website

[![screenshot #1]({{site.url}}/images/free-basics/1.png)]({{site.url}}/images/free-basics/1.png)

[![screenshot #2]({{site.url}}/images/free-basics/2.png)]({{site.url}}/images/free-basics/2.png)

[![screenshot #3]({{site.url}}/images/free-basics/3.png)]({{site.url}}/images/free-basics/3.png)

*Note*: we'll get to the terms of services later on.

## Website optimization

[![screenshot #4]({{site.url}}/images/free-basics/4.png)]({{site.url}}/images/free-basics/4.png)

Okay, this just sounded completely silly. I realize that videos, large images and `.svg`s do take up a reasonable amount of bandwidth, but disabling JavaScript just seemed silly. I had no intention of removing such content from my website nor did I have any intention of re-implementing things and keeping a special fork of the website just so that it follows these guidelines.

After I have read this, I was pretty sure that my website is going to get rejected because it relies on JavaScript to show the navigation bar on small devices and to keep the interface as clutter-free as possible (you know, like 90% of the websites  do nowadays).

## HTTPS support

[![screenshot #5]({{site.url}}/images/free-basics/5.png)]({{site.url}}/images/free-basics/5.png)

Okay, this caching practically breaks my HTTPS support and puts Facebook in control. This means that the users are not going to see my certificate. They're going to see Facebook's certificate and Facebook will then use my certificate to fetch the data from my website. I get completely cut out and Facebook takes over my content, pretending that it is me and that the users are viewing my website. By using Facebook's servers as the proxy, I have absolutely no control over what the users will see. Facebook could manipulate my website in any single way and neither I nor the users of Free Basics are going to know that (since my certificate is no longer being used, users can't in any single way be sure that they're visiting the authentic version of the website).

## Terms of Service

[![screenshot #6]({{site.url}}/images/free-basics/7.png)]({{site.url}}/images/free-basics/7.png)

Surprisingly, they're not as complicated as I thought that they will be. It took me about a minute or two to read them and I was not able to find a single point where I would make a strong objection.

## What happened after I clicked on Submit

I instantly got an email that you can see in the screenshot below:

[![screenshot #6]({{site.url}}/images/free-basics/8.png)]({{site.url}}/images/free-basics/8.png)

Now, all I had to do was wait! Because my website relied on JavaScript, I expected a quick response. That never happened.

Okay, at first, I was really patient because I was aware that I have submitted my request during the holiday season, but, even after the NYE, I still haven't received any response.

Fifteen days later, nothing.

Twenty days later, still nothing.

Now, it's been almost a month. Still, no response from Facebook what so ever.
