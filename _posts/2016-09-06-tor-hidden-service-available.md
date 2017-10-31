---
author: Aleksandar Todorović
comments: false
date: 2016-09-05 16:23:24+02:00
layout: post
slug: tor-hidden-service-available
title: 'Update: Blog now accessible through a Tor hidden service'
categories: en
tags:
- personal
- blogging
image:
  feature: abstract-1-3
---

This blog is now available through a Tor hidden service: `no2ykbljhto2iqgm.onion`.

The hidden service is running on a small VPS (2 x 2.40 GHz CPU, 2 GB RAM), but that's okay I presume since I don't really expect to get a lot of traffic through Tor.

The setup was pretty easy: cronjob every hour that does `git pull` from a [GitHub repo](https://github.com/r3bl/r3bl.github.io), and does `bundle exec jekyll build --destination /var/www/html/`. The website is getting served by an Apache server (it was the simplest solution I could come up with), so there's no need to run Jekyll all the time.

Seems like almost everything works as planned, for now.

The only issue I'm having is that I've used an absolute link far too many times, so some of the links point to my original domain. Will look into fixing that soon-ish.

Oh, and since the original domain is protected by CloudFlare, I have whitelisted Tor so that the users wouldn't be greeted by that god-awful CAPTCHA every time they visit the website. To do this, all I needed to do was to log into CloudFlare, go to `Firewall`, and under the `IP Firewall` tab add Tor as the "country name", and choose to whitelist it.

**Bottom line:** Tor users shouldn't have any difficulties while accessing my website and this website is now (almost) completely Tor-friendly.
