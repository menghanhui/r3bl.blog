---
author: Aleksandar Todorović
comments: true
date: 2015-06-11 20:10:00+01:00
layout: post
slug: elementary-os-workflow
title: "My elementary OS Workflow"
categories: en
tags:
- open source
- elementary OS
image:
  feature: abstract-1-3
description:
---

In this post, I'm going to share with you my workflow and my experience with apps developed specifically for elementary OS. Unfortunately, I'm not very impressed with the state of apps designed specifically for elementary OS right now, but I do think that the situation will improve by the end of the year.

## Web browser

Unfortunately, Midori is not my default browser. Although its design fits elementary OS perfectly, because I'm using some extensions designed specifically for Chrome and Firefox.

Google Chrome and Chromium just look awful on elementary OS. Although I do have Google Chrome installed, but I'm just using some of its web apps from my application launcher. I'm never actually running Chrome.

The browser I'm using is Firefox. Of course, Firefox does not use headerbars nor does it look great on elementary OS, but you can improve that with a couple of extensions.

After I customized my Firefox installation a bit, now it looks like this:

![firefox with one tab open](http://i.imgur.com/IjDBtdQ.png)

If you're wondering where's the tab bar, it's hidden if I have only one tab opened. Once I open two or more tabs, Firefox looks like this:

![firefox with two tabs opened](http://i.imgur.com/J2b9UKi.png)

It ain't much, but it sure beats the hell out of the default Firefox look. If you want to make something similar, here's a [useful tutorial](https://github.com/chpii/Headerbar). Keep in mind that I didn't do all of the steps from it. Although there's still room for the improvement (like creating a custom homepage), I'm quite happy with the current look.

## Email client

Geary just doesn't work well from me. I need a powerful mailing client with lots and lots of options. I have four different email accounts that I check regularly and I need something trustworthy to manage all of them. That's why I'm using Mozilla Thunderbird. I don't think that there's any better email client available for Linux.

I still haven't customized the way Thunderbird looks. It just sits there in the background minimized all of the time until I get a notification that I got a new email.

## Software center

Ubuntu's default software center just looks (and behaves) awful. Unfortunately, I do not have any alternative to recommend right now. I'm just using my terminal emulator to install everything I need. I'm looking forward to the next version of elementary OS (codenamed Loki) that will probably include its own software center.

## Office suite

Apart from the software center, the application that elementary community wants the most is a special office suite. Unfortunately, LibreOffice does not look great by default. You can customize it a bit by installing `libreoffice-style-sifr` package, which will make your LibreOffice look like this:

![libreoffice writer with libreoffice-style-sifr package applied](http://i.imgur.com/BigvEsP.png)

## Text editor

Scratch works great as a basic text editor. Unfortunately, I need something more powerful. I need something that will replace my text editor, my IDE, and my office suite in most of the cases. That's where [Atom text editor](https://atom.io/) kicks in. Here's a picture of me writing this article in Atom text editor:

![picture of me writing this article](http://i.imgur.com/sEaWni7.png)

I'm using [One Dark UI theme](https://atom.io/themes/one-dark-ui) and [One Dark syntax theme](https://atom.io/themes/one-dark-syntax) with [Ubuntu Mono](https://www.google.com/fonts/specimen/Ubuntu+Mono) as my default font.

## Terminal emulator

Once again, the default application (Pantheon Terminal) is great, but I need something where I can split my window horizontally and vertically while I'm doing whatever the hell I'm doing at the moment. That's where [Terminator](http://gnometerminator.blogspot.com/p/introduction.html) steps right in. I made it look semi-transparent so I can see whatever the hell I have opened behind it and it works great. I mostly have a Firefox background in the background which allows me to type the commands from a web resource in my terminal without going `Alt+Tab` all of the time. Here's a picture of my Terminator setup running `screenfetch`:

![terminator running screenfetch](http://i.imgur.com/Zcs8sj1.png)

Oh, and I like to use a green font. It makes me feel like a l33t h4x0r!

## Plank and icon theme

My plank is on the left side and it auto-hides itself. I'm using the left corner of the monitor the least, so that feels like the perfect place for my Plank dock. Here's a picture of my plank:

![my plank](http://i.imgur.com/ILUvZ15.png)

I have only four applications pinned to my dock: Firefox, Thunderbird, Pantheon Files and Terminator. Those four applications are opened all of the time. I run the rest of the apps from Slingshot (I really like the Slingshot launcher).

As for the icon theme, I like the default elementary icon pack. However, since it does not support third-party apps, I like to use [elementary-add](https://github.com/varlesh/elementary-add) icon pack. It combines both elementary's default apps and third party icons that resemble the style of elementary OS.

## Book readers

I love the default Document Viewer shipped with elementary Freya ([Evince](https://wiki.gnome.org/Apps/Evince)). I'm using it regularly to read `.pdf` books. It's simple to use, well designed and low on resources. A picture of Evince with the book called [The Open Organization](http://opensource.com/open-organization) (by Jim Whitehurst, CEO of Red Hat) opened:

![evince running The Open Organization](http://i.imgur.com/xnlevw8.png)

For Kindle books, I just created a web app of Kindle's web interface ([read.amazon.com](https://read.amazon.com/)) using Google Chrome. It works great and it feels very well designed! Here's a picture of it with the book called [L.A.I.R.A. 1st Evolution, Rising](http://www.amazon.com/L-I-R-1st-Evolution-Rising-ebook/dp/B00N9O7SCC/) (by John J. Sanders) opened:

![kindle web app](http://i.imgur.com/7XQ7kvO.png)

## Music player

I'm running elementary's default app (called Noise) to play files from my hard drive. But most of the time, I'm using [Spotify for Linux](https://www.spotify.com/us/download/linux/). It ain't perfect, but it gets the job done.

## Video player

For the videos and movies, I'm using [Popcorn Time](https://popcorntime.io/) and [VLC](http://www.videolan.org/vlc/). Audience (elementary's default) is great, but I got used to VLC's features and I've been using it for years (I was using it back in my Windows days too).

## Other apps I'm using

* [qBittorrent](http://www.qbittorrent.org/) for managing my torrent files.
* [VirtualBox](https://www.virtualbox.org/) for managing my virtual machines.
* [HexChat](https://hexchat.github.io/) as the IRC client.
* [Pidgin](http://pidgin.im/) to chat with my Firefox friends.
* [MEGAsync](https://mega.co.nz/) as a cloud service.
* [Mark My Words](https://github.com/voldyman/MarkMyWords) to write articles for other sites (like [Opensource.com](http://opensource.com/) and [Kompjuteraš](http://kompjuteras.com/)).

## My overall satisfaction

To be honest, I'm not very satisfied with the third-party apps developed specifically for elementary OS (for now). The only applications I'm using regularly are [elementary-tweaks](https://launchpad.net/elementary-tweaks) and [Mark My Words](https://github.com/voldyman/MarkMyWords). Also, [Go For It!](http://manuel-kehl.de/projects/go-for-it/) is great, but I don't need most of its features. I just use [language-todotxt](https://atom.io/packages/language-todotxt) Atom package to manage my to-do list.

I really do hope that more developers will switch to making applications for elementary OS. I think I will try to make some as well after my summer exams (like a well-designed `.epub` reader that I think Linux desperately needs).

## Some other links

* If you want to find a list of third-party applications developed specifically for elementary OS, go [here](http://hdw.eweb4.com/out/976720.html) or [here](http://madeforelementary.tumblr.com/).
* If you're wondering where you can find my wallpaper, it's [here](http://hdw.eweb4.com/out/976720.html).

If you have any questions about my setup, feel free to leave a comment. I'll be more than happy to help you out.
