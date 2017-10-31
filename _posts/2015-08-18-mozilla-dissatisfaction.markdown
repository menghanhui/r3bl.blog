---
author: Aleksandar Todorović
comments: false
date: 2015-08-19 01:10:00+01:00
layout: post
slug: mozilla-dissatisfaction
title: "Why my dissatisfaction with Mozilla is increasing"
categories: en
tags:
- Mozilla
- Firefox
- rant
image:
  feature: abstract-1-3
---

I was a big fan of Mozilla not too long ago. Somewhere around four years ago, I have decided to slowly make the switch to open source software. Naturally, switching from Chrome to Firefox was the first switch I made.

It felt... empowering. Firefox seemed perfect at the time. It didn't feel like a downgrade, it felt like an upgrade! I was more than hyped about it.

In the meantime, Chrome improved a lot. Firefox... well, it made some cool changes, but the advancement seemed highly slow compared to Chrome. Of course, Mozilla doesn't have a huge company behind it like Chrome has and I understood that. I remained loyal to Firefox and I was perfectly happy with it.

Recently, that hype I was feeling started fading. First, there was that sync feature. I trust Mozilla with my data so I singed up for sync. It promised to sync everything (including my preferences), but it really didn't. I like my interface small and minimalistic, so I like to remove the features I'm not really using on a daily basis from the interface. Firefox's sync... well, doesn't sync the look of my interface, so every time I reinstall it or install it on a new device, I have to hide those features all over again.

Then there was that Pocket integration. I am a Pocket user. I was a Pocket user for a long time before Firefox integrated it. It's a nice web app that I liked and used for quite a while. But bundling it with my open source browser out of the box seemed... wrong. No matter how much I liked Pocket, it's a proprietary service. Sure, I could turn it off and because of the rage I was feeling at the time, I did. I also stopped using Pocket for a couple of weeks. Okay, I figured out that Mozilla has to find a way to make money and stop relying on Google, so I eventually cooled down and started using Pocket all over again. But still, it feels... wrong.

During the upgrade to the version 39 (if I'm not mistaken), on my brother's computer, Firefox changed his search provider to Yahoo. It was a mistake I presumed because only a small fraction of users encountered it. Okay, I could live with that too. I just changed the search provider on my brother's computer back to Google (I myself am a DuckDuckGo guy).

I'm running the beta version of Firefox. It's as stable as the stable version of Firefox is in my experience. So, tonight, I upgraded Firefox to the version 41 and that's when I encountered yet another problem.

I don't like Firefox's new tab page. I was looking for an alternative add-on that could satisfy my needs, but I couldn't find one. So, I created a HTML document and decided to make myself a new tab page myself. I had successfully done so and my current new tab page looks like this:

![my custom new tab page](http://i.imgur.com/DUvqsnI.png)

It's nothing special because... well, I don't need nothing special. It's basically a modified [Tactile theme](https://github.com/jasonlong/tactile-theme), one of the themes that you can select in GitHub's web page creation wizard. The code is, of course, [publicly available](https://github.com/aleksandar-todorovic/firefox-custom) and the page is accessible [on my website](http://r3bl.me/firefox-custom/), although I'm linking to the `.html` from my local machine because... well, it's faster.

But, when I upgraded to the version 41 tonight, Firefox switched back to its original new tab page. I checked my `about:config` and the `browser.newtab.url` was still pointing to the correct location of my `.html` file.

Okay, another error I thought, so I have decided to contact Mozilla's support. While I was typing my question, I discovered that this question [was already asked](https://support.mozilla.org/en-US/questions/1077559). As it turned out, they have decided to ditch that setting because those pesky bloatware softwares were abusing it.

Okay, so that question did let me know about the [bug report](https://bugzilla.mozilla.org/show_bug.cgi?id=1118285) so I thought I should look it up myself. As it turned out, this issue was fixable by installing yet another add-on. But what was mind boggling to me was that _every single comment_ that was against this switch was flagged as either `off-topic` or `advocacy` (whatever the hell that means) and as a consequence, it was hidden from the discussion. The fuck?

Again, it just feels... wrong. Sure, I understand that this fixes the problem for those users who are using Windows and blatantly clicking next during the installation process, but I'm a freaking Linux user. I haven't encountered any bloatware in years! But as it turned out, I have no say in this. Neither does anyone else who's against this change.

It seems to me like there's some issue that I need to fix every freaking time I update my Firefox. I don't have any valid alternative to switch to neither. Sure, Chromium is open source, but it still feels like I'm using Google's product.

So the only solution seems to continue to use Firefox for now. But I am no longer thrilled about using it. I just feel like... I need to.

And then, there's Thunderbird. Thunderbird is without a doubt still the best emailing client you can get on Linux, but Mozilla decided to stop developing it. The last version available from `apt-get` is the version 31 for god sake.

Four years ago, I was thrilled when I switched to Mozilla's products. Now, I feel more and more disappointed as the time goes by. That doesn't seem right! The Mozilla Foundation was supposed to be the role model for the open source world!

Now, it feels opposite. I hope other open source projects will stop looking at Mozilla as a role model. They seem to be making a mistake after a mistake. Maybe instead they should look at LibreOffice and The Document Foundation as a new role model? At least those guys seem to know what they're doing. At least they're not disappointing me with their decisions...

![random image I found on the interwebz](http://www.quickmeme.com/img/d8/d8e162ce769d7e4fd5335aec8dcde859a842fc4d082ad6f33ee412e7e51e8b79.jpg)
