---
layout: post
title: "Privacy Policy"
permalink: /en/privacy-policy/
redirect_from: /privacy-policy/
comments: false
share: false
image:
  feature: abstract-1-3
---

<div style="text-align: center;"><small><strong>Effective from:</strong> {{ page.git.last_commit.commit_date | date: '%B %d, %Y' }} // <strong>Latest changes:</strong> <a href="https://code.r3bl.tech/sites/r3bl.blog/commit/{{ page.git.last_commit.long_sha }}?style=split">{{ page.git.last_commit.short_sha }}</a></small></div>

<hr/>

## Statement

As the owner of the website, I do my best to protect the privacy of you as my visitor at all times.

* I don't store any personally identifiable data about you as my visitor.
* The website is hosted on a dedicated server I have control over. The server in question is under the EU jurisdiction, obliging both me and my provider to the highest privacy standards.
* I don't serve ads. Instead, I [promote projects I support](https://r3bl.blog/en/relevant-content/) by randomly picking one of them to display to you at the bottom of the page.
* I try to prevent your browser from making unnecessary connections outside of my control.

## Applies to

This privacy policy applies to the following domains:

* [r3bl.me](https://r3bl.me)
* [r3bl.blog](https://r3bl.blog)
* [r3bl.dj](https://r3bl.dj)
* [r3bl.tech](https://r3bl.tech) (under construction, release TBA)
* [netneutralnost.com](https://netneutralnost.com)

#### Analytics

I self-host my own analytics service called [~~Piwik~~Matomo](https://matomo.org/). In a nutshell:

* It's not hosted by Google nor any other third party.
* It is configured in such a way that it respects [Do Not Track](https://en.wikipedia.org/wiki/Do_Not_Track) preference. If you chose not to be tracked in your browser's preferences, you will not be tracked.
* Connections to it are blocked by all adblockers that have the [EasyPrivacy](https://easylist.to/#easyprivacy) list enabled ([uBlock Origin](https://github.com/gorhill/uBlock/#installation) has it enabled by default).
* I obscure the IP addresses of where you're coming from to two bytes. Instead of seeing `88.198.121.205` (in case you're wondering: IP address of the server hosting the sites), I only see `88.198.XXX.XXX`.

**What this means:** I cannot associate the collected data with you as an individual in any way. While you could approach me and give me enough data to uniquely identify you in the database, you should know that I do not have enough data to know who you are without you identifying yourself. I've made sure to comply with the [guidelines by Matomo](https://matomo.org/blog/2018/04/how-to-not-process-any-personal-data-with-matomo-and-what-it-means-for-you/) in order not to store any personal data.

**What I do with data:** I use them to track where the visitors are coming from, what are they visiting, how long are they using the website, and what kind of a device are they using to access the website. I collect very minimal, easily avoidable insight in order to improve the speed of the website and to have some general idea as to how far my word reaches. I sometimes boast about the overall numbers and make some inner decisions based on the stats.

**What third parties do with the data:** Nothing. Third parties don't have access to such data.

### General Data Protection Regulation (GDPR) compliance

As all the data I collect is anonymous ([recital 26](https://gdpr-info.eu/recitals/no-26/)), and used solely for my personal use ([recital 18](https://gdpr-info.eu/recitals/no-18/)), I do not require consent from you in order to collect and process such data. Since I do not share the collected data with any third party, I am a sole data processor of the collected data.

### Updates to the privacy policy

Since I don't know who you are, I cannot send you an update whenever I make changes to my privacy policy. As a way around that, I am providing you with the date from which the current version of the policy is effective ({{ page.git.last_commit.commit_date | date: '%B %d, %Y' }}), together with the last Git commit that made changes to the text of the policy ([{{ page.git.last_commit.short_sha }}](https://code.r3bl.tech/sites/r3bl.blog/commit/{{ page.git.last_commit.long_sha }}?style=split)), enabling you to see the changes I've made side-by-side.

## What I don't do on this website

* I do not sell nor share any data I collect.
* I do make money on this site by serving ads or mining cryptocurrencies.
* If I ever decide to publish some sponsored content, I will make sure it's easy to distinguish as such.
* I do not use Google Analytics, Google Fonts, Google's CDN, etc. I am one of the signatories of the [anti Google AMP letter](http://ampletter.org/), and have strong opinion against sharing your data with the company that's pushing for AMP.
* I do not make connections by default to any social network. When you see a button or a link to it, please be aware that your browser will not make a connection to it by default. In order for the connection to be made, you have to make an explicit action showing your intention of making a connection to it (by clicking on it).

## What do I do to make my content easy to consume

* I make my websites as fast and as minimalistic as possible.
* I focus on the content first. Everything else gets out of the way.
* I carefully structure my data so that it's easily recognizable to search engines (and scrapers)..
* I make sure my articles look good using browser's reader mode and [Pocket](https://getpocket.com/).
* I use descriptive alt tags in images.
* I use [Open Graph](http://ogp.me/) and Twitter Cards, making my content look nice when it gets shared.
* My blog is available [over RSS](https://r3bl.blog/feed.xml). My RSS feed returns full articles (not just excerpts), making visitors able to read my content in its entirety using their favorite RSS reader.

## How does this website earn money?

It doesn't.

However, maintaining my infrastructure which runs my sites costs me a considerable amount of money (~40€/month). You can help me cover my costs by making a [one-off donation using PayPal](https://www.paypal.me/r3blme), or [recurring donations using Liberapay](https://liberapay.com/r3bl).
