---
author: Aleksandar Todorović
comments: false
date: 2017-04-27 11:30:00+01:00
layout: post
slug: chrome-vs-chromium
title: "Chrome is basically crippling Chromium's features"
categories: en
tags:
- technology
- rant
- browsers
- open-source
image:
  feature: abstract-1-3
---

TIL that installing Chrome on Ubuntu effectively messes up some Chromium features that worked just fine previously. Here's what happened.

After running Chromium for a while, I've decided to try switching over to Chrome. So, I've downloaded their `.deb` file from [their official website](https://www.google.com/chrome/browser/desktop/index.html), installed it via `sudo dpkg -i <FILENAME>.deb`.

Since I'm a heavy user of at least one Chrome/Chromium app — [Signal](https://chrome.google.com/webstore/detail/signal-private-messenger/bikioccmkafdpakkkcpdbppfkghcmihk) desktop client — and I always have it running in the background, I've noticed that installing Chrome closed Signal. Once I've tried relaunching it, I've got greeted with the screen asking me to pair my device:

![Signal device pairing screen](https://support.whispersystems.org/hc/en-us/article_attachments/204262718/Screenshot_from_2015-11-28_22_37_18.png)

That's... weird.

One more thing I've noticed is the whole Signal interface looks rather tiny compared to what it used to be. I remember manually modifying HiDPI settings in the `.desktop` files by including the `--force-device-scale-factor=1.2` flag in the `Exec=` lines and it seemed it's no longer working.

A quick look at my `~/.local/share/applications/` folder (which ~~is~~ _was_ a folder where Chromium stores its `.desktop` files) revealed that the Chrome actually modified every `Exec=` line in that file in order to run Chrome apps with Chrome, instead of Chromium. Since they keep two separate databases, I've effectively lost my entire Signal history on my laptop.

...well, okay, not exactly. Quick change to the `.desktop` file and manually re-adding Chromium's executable instead of Chrome's executables would probably fix that, but since in the moment of panic I have already unlinked the Signal device from my smartphone, it really didn't matter at that point.

At that point, I've realized that having Chrome installed might not be the best idea ever. So I did the following:

```bash
dpkg -l | grep "chrome"
dpkg -r google-chrome-stable
```

After that, I've just wanted to continue using Chromium. Just to be extra sure, I've removed `.desktop` files from `~/.local/share/applications`, hoping that re-triggering shortcut creation would fix that problem.

But, alas, Chromium is no longer able to save the files over to `~/.local/share/applications`. Creating shortcuts no longer works from Chromium.

Here's me deciding to install a random Chromium app just to make sure:

![le random Chromium app](https://raw.githubusercontent.com/r3bl/r3bl.github.io/master/images/chrome-chromium/1.png)

And here's what's listed in `~/.local/share/applications` after installing it (note: the `.desktop` file should be named `chrome-delkpojpfkkfgmknffmblbhmlamkjioi-Default.desktop`):

![le random Chromium app didn't create a .desktop file](https://raw.githubusercontent.com/r3bl/r3bl.github.io/master/images/chrome-chromium/2.png)

Also, every single time you open Chromium, you're asked if you want to set it as a default browser (I want to), but clicking on "yes" doesn't really do a thing (after clicking it for a couple of times, I went into GNOME's settings and just changed my default browser there).

I've looked back at my terminal history and made sure I haven't removed any packages related to Chromium once I uninstalled Chrome. Nothing showed up.

So, I've been stuck with this inability to use Chromium properly, and not having Chrome installed. Because I didn't know what else to do, I've decided to install Chrome again.

Of course, Chrome is now capable of storing `.desktop` files in `~/.local/share/applications`. Chromium is not. I've effectively lost my entire Signal library in the process and am unable to use Chromium in the way I did before.

And no, Chrome's sync feature and Chromium's sync feature are apparently not the same thing, so I now have to re-download all Chromium apps as Chrome apps and I don't see any way of getting rid of Chrome from my Ubuntu installation and reverting back to using Chromium exclusively.

Whichever engineer decided that modifying `.desktop` files created by another application during the installation is a smart idea should rot in hell.

This is basically a dark pattern lite.
