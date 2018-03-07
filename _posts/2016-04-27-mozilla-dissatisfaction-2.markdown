---
author: Aleksandar Todorović
comments: false
date: 2016-04-27 01:10:00+01:00
layout: post
slug: mozilla-dissatisfaction-part-2
title: "Why my dissatisfaction with Mozilla is increasing — Part 2"
categories: en
tags:
- rant
- technology
- advocacy
image:
  feature: abstract-1-3
---

I have already talked about [why my dissatisfaction with Mozilla is increasing](https://blog.r3bl.me/en/mozilla-dissatisfaction/) about 8 months ago. In that blog post, I mentioned Firefox Sync, Pocket integration, automatic switch to Yahoo as the default search engine (in the minority of cases, of which one was in my family), disregarding power user's needs to focus on Windows idiots who blindly click on "Next", and the overall ignoring the fact that Thunderbird is (probably) the second most popular Mozilla product to this day (more on that later). A lot of changes happened since that original post and my dissatisfaction only kept increasing, so I decided to write part two about the same topic.

![]({{ site.url }}/images/misc/NlaXK64.jpg)

Okay, so the Mozilla guys first tried to explain to us that they're not really going to focus on developing new Thunderbird features so they could focus on Firefox and said to us that they're preparing something big. That big thing turned out to be Firefox OS. Okay, sure. I would _love_ to have a Mozilla developed OS on my phone. Then, a gigantic amount of time passed and I was still waiting for Firefox OS to enter the market in my country. Nothing happened.

Then, Mozilla signed a contract with a carrier in a country right next to mine and I had hope once again that I'll be a proud Firefox OS owner in no time. At that time, I was not a smartphone user simply because I cared about my privacy too much to have it handed over to Google or Apple. I felt... left out. Ubuntu Mobile was barely a thing and no open source project really managed to make it easy for me to buy a phone running a truly open operating system. I had my hopes high on Firefox OS becoming available in my country and Mozilla managed to let me down. Finally, in August last year, I had to give up on my decision of not using Android or iPhone and bought an Android powered phone because it's the closest thing I could get to an open source operating system.

Then, Mozilla announced that they're shifting Thunderbird completely to the community so that they could focus on Firefox. Okay, I respected that decision... for about two days.

About two days after they made that announcement, in December 2015, they released [Focus](https://itunes.apple.com/us/app/focus-by-firefox-content-blocking/id1055677337?mt=8) for iOS. Focus has _nothing to do_ with the Mozilla's mission of promoting the open Web what so ever. It's a freaking productivity tool that works with Safari (and _exclusively_ with Safari)! Now I was _really_ starting to get pissed!

Then, before I actually managed to get my hands on one of Firefox OS powered smartphones, they told us that they're killing the whole idea of Firefox OS for smartphones and changing its course to Internet of Things. They also said that they have no plans of signing any more contracts with the carriers. And then, I was just furious! In the Hacker News discussion about the whole switcharoo of Firefox OS to the IoT, I posted the following comment out of anger:

> So, at first, they've told us that they don't have enough resources to pour into Thunderbird because they were working on something else. That something else was Firefox OS. Okay, sure. I would love to have a Mozilla developed OS on my phone. Then, months have passed and, even though they have an agreement with the country right next to mine, I was not able to have one without having someone from that country who will sign a contract with the carrier. Then they have decided to give Thunderbird away to some other project because they wanted to focus on Firefox. Sure, why not? But, a day or two later, they have released an app for iOS that completely does not belong in their model of service since it has nothing to do with Firefox and it won't actually work with Firefox. And now they're telling us that they're moving Firefox OS to "IoT devices", killing Firefox OS smartphone idea before I had a chance to actually get my hands on one of them. Great work Mozilla!

I expected people to downvote me because I was not really boosting the discussion with my comment, but instead, it became the top comment on that thread, which proved me that I'm not the only one feeling frustrated with Mozilla (or at least with Mozilla's decisions).

## Meanwhile...

Meanwhile, none of the things I talked about in the previous rant were actually fixed. Firefox Sync still doesn't... well, sync. At least not properly. Every time I install Firefox somewhere else, I still have a lot of tweaking to do. Like, getting rid of the search bar because it's completely useless and hiding ten more extension icons down to the hamburger menu because, for example, I really don't care about how many trackers has [Privacy Badger](https://www.eff.org/privacybadger) blocked — all I care about is that it blocked them. But nope, my choices of customizing the interface do _not_ get synced with Firefox Sync at all.

And the Pocket integration is still there. I am an avid user of its service. In fact, I turned out to be in the top 5% of their users in 2015:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">I might be addicted to <a href="https://twitter.com/Pocket">@Pocket</a>. <a href="https://t.co/Oz3ED2DR0i">pic.twitter.com/Oz3ED2DR0i</a></p>&mdash; Aleksandar Todorović (@r3bl_) <a href="https://twitter.com/r3bl_/status/694949974602285056">February 3, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

However, I am still frustrated by the fact that Mozilla decided to integrate a proprietary service to their open source browser. I would have downloaded the add-on by myself for sure. But having it pre-installed is just wrong. And no, the fact that it doesn't really send any requests to Pocket until you click on the icon doesn't really do much considering that this is one of the features that Firefox _loves_ to emphasize once you install it, together with Firefox Hello.

And then, there was the whole charade with _why_ exactly _did_ Firefox decide to add Pocket. First, a Mozilla employee [made a post in /r/firefox](https://www.reddit.com/r/firefox/comments/38aorv/psa_mozilla_is_not_benefiting_from_the_pocket/) in which he said that Mozilla received no monetary compensation from Pocket.

Turns out that Mark Mayo, Mozilla's VP and GM of Firefox, actually confirmed this in an email sent to the mail developer of [Wallabag](https://www.wallabag.org/), which is, simply put, a self-hosted version of Pocket. In that email, Mark [said](http://www.planet-libre.org/?post_id=18514):

> To be clear, though, this has absolutely nothing to do with money. We're shipping Pocket because we love their product, and so do our users.

Am I crazy for thinking that incorporating a proprietary service into an open source browser just because the developers like the service? This doesn't make any sense to me!

Then, [WIRED published an article](http://www.wired.com/2015/12/mozilla-is-flailing-when-the-web-needs-it-the-most/) in which it stated:

> Although the company emphasizes that Pocket and Telefonica didn’t pay for placement in the Firefox browser, Mozilla Corp. chief legal and business officer Denelle Dixon-Thayer told WIRED that Mozilla has revenue sharing arrangements with both companies.

So technically, they're not actually profiting from the Pocket integration. Pocket is the one who is profiting from the Mozilla's decision to include a proprietary service in its browser.

Okay, now Mozilla's decision officially managed to make even less sense.

Meanwhile, Firefox Hello, a really cool feature that nobody asked for and probably nobody's using is still there.

By the way, I still have to rely on an [add-on](https://add-ons.mozilla.org/en-US/firefox/add-on/new-tab-override/) to get the old `browser.newtab.url` feature.

But the whole logic behind this shift is just killing me. It's an add-on developed by someone who is closely tied with Mozilla that replaces the old functionality and still functions just like `browser.newtab.url` did. And the add-on is released under the MIT license. So, what's really stopping bloatware developers from redoing what this add-on does?

A couple of days ago, I stumbled upon a bloatware on my brother's machine that opened a custom web page every time Firefox starts. I checked Firefox extensions. Nothing out of the ordinary happened there. Since he's using Windows 10, I checked Control Panel -> Programs and Features. Nothing suspicious going on there neither. I tried reproducing the build by quitting Firefox and starting it from the taskbar and the behavior didn't reproduce. Then, my brother pointed out to me that this thing happens when he clicks on the desktop icon, not the taskbar icon. And he was right.

Turns out that the bloatware tweaked the command that the shortcut was executing. Instead of just calling Firefox, the shortcut also passed the URL to the bloatware site. So, every time you clicked on the desktop shortcut, Firefox will start normally, restore all of the tabs from the previous session, but also open up a new tab and load the bloatware site. I have to say that this was a highly interesting and pretty original approach in my book.

This is just one of the examples how the removal of the `browser.newtab.url` feature actually didn't accomplish much in protecting the ones who just click on the button "next" without actually reading anything.

## Thunderbird

I really can't criticize Mozilla without mentioning Thunderbird. It's still a much needed app. It's still the only multiplatform-supported program that works well with GPG encryption. It's still the only usable alternative to Outlook.

Since the beginning of 2015, there have been two blog posts posted on Thunderbird's blog about how many people are actually using Thunderbird. The first one [dates back to February 2015](https://blog.mozilla.org/thunderbird/2015/02/thunderbird-usage-continues-to-grow/) and shows us that the number of daily Thunderbird users on February 24th 2015 was exactly 9,255,280. In that post, there's also a nice graph of the Thunderbird usage increase which proves that this is not an isolated date:

![thunderbird usage graph](https://ffp4g1ylyit3jdyti1hqcvtb-wpengine.netdna-ssl.com/thunderbird/files/2015/02/Thunderbird_ADI_2018-2015.png)

To quote the blog post, this graph represents the "number of pings that Mozilla servers receive as installations do their daily plugin block-list update".

This growth apparently continued because on December 9th 2015, there was a new [update](https://blog.mozilla.org/thunderbird/2015/12/thunderbird-active-daily-inquiries-surpass-10-million/) on the Thunderbird's blog letting us know that the November 30th 2015 was the very first day in which over 10 million people used Thunderbird.

So, Thunderbird currently has ~10 million daily users. I took a quick look at how successful Firefox is on Android. It turns out it has between 100 and 500 million downloads and about 2.3 million reviews on Google Play. Now, iTunes does not provide me with the approximate number of downloads, but considering that it currently has only 26 ratings and that it was released about half a year ago, I'd say it doesn't have over 1 million daily users.

If we put all of these statistics together, it's pretty certain that Thunderbird is either the 2nd or the 3rd most popular product that Mozilla has (depends on the number of daily Firefox on Android users, for which I was not able to find an estimate). So, why is Mozilla so eager to pass it to someone else?

[Nylas N1](https://github.com/nylas/N1), although not a classic emailing client per se since it requires using the server for parsing the documents (which could be Nylas' or self-hosted), managed to prove us that there's still a need for a beautiful and customizable open source desktop emailing client. I didn't manage to get any better statistics on its usage than the number of GitHub stars, which it currently has over [17 thousand](https://github.com/nylas/N1).

With both Thunderbird and N1 going pretty strong and attracting new users on a daily basis, it seems like the idea of a desktop emailing client is still going pretty strong. Predictions of the desktop clients losing relevance today thanks to a huge amount of people using browsers or smartphones to check their emails still seems empty. Yet, Thunderbird's future still remains a mistery.

Two days ago, Mark Surman, Executive Director at Mozilla, posted a blog called [Firefox and Thunderbird: A Fork in the Road](https://marksurman.commons.ca/2016/04/25/firefox-and-thunderbird-a-fork-in-the-road/). However, what was more interesting to me than the blog post itself was [a report](https://blog.mozilla.org/thunderbird/files/2016/04/Finding-a-Home-for-Thunderbird.pdf) (warning: PDF) about Thunderbird's future.

In that blog post, they're mentioning a bunch of projects that were approached by Mozilla. The two most likely options:

* [Software Freedom Conservancy](https://sfconservancy.org/) has already shown full interest in taking over the project completely, however, it was never in charge in anything as large as this project is, which means that the Thunderbird would be their biggest project from day one.
* [The Document Foundation](http://www.documentfoundation.org/), for which I stated in the previous post about this topic that I hope will be the organization that will take Thunderbird under its arms, is apparently interested in hosting Thunderbird, but not incorporating it as an integral part of LibreOffice.

I'm rooting for the second one, since I really do have a faith that The Document foundation is able to continue on the path where Mozilla left off, both as the Thunderbird maintainers and as the true example of the successfully run open source organization.

I'm both concerned and excited at the same time. I really do hope that Mozilla will be extra careful about this decision. 10 million people depend on it. But I wouldn't be too surprised if Mozilla manages to let me down once again and gives away Thunderbird to someone like Apache (who hasn't been formally approached by Mozilla, according to the same report).
