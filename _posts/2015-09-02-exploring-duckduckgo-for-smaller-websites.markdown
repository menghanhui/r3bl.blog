---
author: Aleksandar Todorović
comments: false
date: 2015-09-02 17:00:00+01:00
layout: post
slug: exploring-duckduckgo-for-smaller-websites
title: "How to get indexed on DuckDuckGo if you're running a smaller website"
categories: en
tags:
- technology
- tutorial
image:
  feature: abstract-1-3
---

My favorite search engine is [DuckDuckGo](https://duckduckgo.com/), there's no doubt about that. So, I wanted my site to be indexed by my favorite search engine. My website is rather small (judging by the [current Alexa rank](http://www.alexa.com/siteinfo/r3bl.me) it's not even in the top 15 million sites out there), so, let's see what I can do.

![DuckDuckGo](https://upload.wikimedia.org/wikipedia/en/thumb/5/55/DuckDuckGo_Logo_%28mid_2014%29.svg/1280px-DuckDuckGo_Logo_%28mid_2014%29.svg.png)

Unlike other search engines, DuckDuckGo doesn't offer any kind of webmaster tools. They don't have any kind of a crawler that is going to crawl your website. To index your site, you have to rely on the search results from other search engines and come up with a way to index your site.

So, my first step was to index my site on Google using [Google's webmaster tools](https://www.google.com/webmasters/). This was by far the easiest process. I thought that if my site was indexed by Google, it surely can be accessed using DDG. Boy, was I wrong!

[Indexing my site on Google](https://encrypted.google.com/search?hl=en&q=site%3Ar3bl.me) was easy. Currently, Google has indexed 227 pages from my domain. But still, when I type `site:r3bl.me` using DuckDuckGo, DDG returned me 0 results.

Okay, so I searched DDG's forum a little and as it turns out, they're suggesting to submit your site to Yahoo! and Bing instead. If it gets indexed by those search engines, your site should be accessible via DuckDuckGo.

Unfortunately, that wasn't the case. Currently, Yahoo doesn't offer webmaster tools. If you visit [this link](http://search.yahoo.com/info/submit.html), they're going to suggest you to use Bing's webmaster tools instead.

So, I submitted my site to [Bing's webmaster tools](http://www.bing.com/webmaster/). Bing has successfully indexed 16 pages of search results for my site, but _still_, if I typed `site:r3bl.me` I got 0 results.

Then, I remembered [Yandex](https://www.yandex.com/). For those of you who are not familiar with Yandex, it's the most popular Russian search engine. I remebered that DuckDuckGo has a partnership with Yandex. So, let's give Yandex a try.

As it turns out, I was right. When I tried searching for `site:r3bl.me` using Yandex, I got 0 results.

Luckily, Yandex does offer [webmaster tools](https://webmaster.yandex.com/). So, I submitted my website. But Yandex indexed my site far longer than Google and Bing did. Once you submit your site, they warn you that the indexing process might last for a week or two. And they're not kidding! It took almost two weeks, but my main [r3bl.me](https://r3bl.me) domain _was_ indexed by Yandex.

The same applied instantly to DDG. Now, when I search `site:r3bl.me` [on DuckDuckGo](https://duckduckgo.com/?q=site%3Ar3bl.me), the search results are the same as the results I get when I'm doing the same search request on Yandex.

So, Yandex's search engine _was_ the key to the puzzle.

So, if you're running a small website and you want it to be indexed on DDG, forget about Google, Bing and Yahoo. Get your site indexed on Yandex instead.

Unfortunately, three results that I currently get are far from enough. So, about an hour ago, I have submitted a request to Yandex to index my [r3bl.blog]({{site.url}}) subdomain as well. Once that process is done, my website is going to be accessible through both DuckDuckGo and Yandex.

**tl;dr**:

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Have a small site that you want to index in DuckDuckGo? Forget about Yahoo and Bing. Use Yandex&#39;s webmaster tools: <a href="https://t.co/3aZSYhXTY1">https://t.co/3aZSYhXTY1</a></p>&mdash; Aleksandar Todorović (@r3bl_) <a href="https://twitter.com/r3bl_/status/639079263212318720">September 2, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
