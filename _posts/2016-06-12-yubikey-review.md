---
author: Aleksandar Todorović
comments: true
date: 2016-06-12 00:50:00+01:00
layout: post
slug: mozilla-dissatisfaction-part-2
title: YubiKey NEO: Ubuntu 16.04 usefulness (+ review)
categories: en
tags:
- YubiKey
- Firefox
- rant
image:
  feature: abstract-1-3
---

I got a hold of a [YubiKey NEO](https://www.yubico.com/products/yubikey-hardware/yubikey-neo/), so I was wondering how useful it is and what can I do with it. Here's my "tutorial" on setting it up using Ubuntu 16.04 and actually using it.

![YubiKey NEO](http://www.hotforsecurity.com/wp-content/uploads/2012/08/Yubikey-NEO.jpg)

## Installation instructions

First of all, `yubikey-neo-manager` _is_ available through the default software sources, but since I wanted to avoid waiting for the Ubuntu guys to review the new versions of the package, I've decided to go with the [official PPA](https://launchpad.net/~yubico/+archive/ubuntu/stable) and installed `yubikey-neo-manager` using the following commands:

```bash
sudo add-apt-repository ppa:yubico/stable
sudo apt update
sudo apt install yubikey-neo-manager
```

All set!

Worth pointing out: to execute the package, you don't run `yubikey-neo-manager` as a command (as one would have thought). Instead, what you should be running is `neoman`.

So, once installed, I ran `neoman` and clicked on `Change connection mode` so I could enable the CCID mode because I read somewhere that this might be helpful later on.

Now I'm off to see what this baby can do!

The [Why Yubico -> For Individuals](https://www.yubico.com/why-yubico/for-individuals/) page tells me that I can use my Yubico to enable 2FA on a half a dozen of online services:

* Gmail and Google Accounts
* GitHub
* Dropbox (using U2F)
* LastPass Premium
* Dashlane Premium
* WordPress

What I noticed, however, is that every time I tried to set up any of these services, what I've discovered is that they all require me to use Google Chrome. I'm a hardcore Firefox fan, so that wasn't an option.

A little bit of DuckDuckGo magic and I've discovered this addon: [U2F Support Add-on](https://addons.mozilla.org/en-US/firefox/addon/u2f-support-add-on/). Great! Just what I needed!

## GitHub setup

After I installed this addon, I've set up GitHub's 2FA using [Google Authenticator](https://en.wikipedia.org/wiki/Google_Authenticator) (I needed to enable _some_ 2FA method to be able to configure it later with my YubiKey), and then configured my YubiKey by visiting https://github.com/settings/two_factor_authentication/configure, clicking on `Register new device` on the bottom of the page and then simply pressing my YubiKey.

After that, I logged out, tried logging back in, and I was negatively surprised because GitHub, by default, wants me to log in using Google Authenticator and I need to click on one more label to use the security key verification, after which I need to tap the button on my Yubikey.

Minor inconvenience, but I can work with that.

## Google / LastPass / Dropbox issues

Unfortunately, Google's 2FA refuses to allow security keys as a method for verification if you're using anything else except Google Chrome, even though my Firefox installation now fully supports U2F protocol thanks to the addon I've installed. Same thing applies to Dropbox.

As for the LastPass, I refuse to pay for a premium account to be able to use extra security. I'm in a constant love-hate relationship with the LastPass service, but this is where I draw the line. If you don't allow me to use my Yubikey without a premium account, you're losing me as a consumer. Dashlane is another password keeping service that supports 2FA using Yubikey, but it is not available on Ubuntu (no, I'm not installing `wine` for this), so it's not for me.

At the end, I've decided to go with `keepass2` and accepted the fact that I'll spend the next hour getting it to work properly.

## KeePass2 integration

So, after I did `sudo apt install keepass2`, I've spent like half an hour exporting my data from LastPass, realizing that they're saved as `.html` instead of `.csv`, renaming the file to `.csv`, importing them into KeePass2, crying when I figured out that I need to install `mono-complete` to be able to use KeePass plugins... I was ready to go.

So, about 15 minutes after executing `sudo apt install yubikey-personalization-gui mono-complete` and sobbing while my system installed the entire Mono framework, I've downloaded two [KeePass2 plugins](http://keepass.info/plugins.html): OtpKeyProv and KeePassHttp. After I figured out that the KeePass plugins should go into `/usr/lib/keepass2/`, I realized that it is time for me to use `yubikey-personalization-gui` package.

Settings the YubiKey with KeePass2 up wasn't really an easy job, so I'm just going to [leave the official tutorial here](https://www.yubico.com/why-yubico/for-individuals/password-managers/keepass/).

**Warning:** If you don't want to make the same mistake as me, be sure to copy your secret key somewhere (which will come in HEX form) _before_ closing `yubikey-personalization-gui`, because I was not able to find the secret key after re-opening the personalization tool. You'll need to paste it into KeePass2 settings later in the process.

So, that should be it!

The tutorial tells me that I'll have to create "3 consecutive passcodes (one for each bar) by pressing the button on your YubiKey for three seconds". Typing in a 40 character long master password and then pressing the YubiKey three times for three seconds sounds a bit time consuming, but okay.

Unfortunately, what I've discovered is that sometimes YubiKey just refuses to generate a passcode even after three seconds. I have to press it like 5 times for three seconds to get three passcodes and to finally be able to login.

## Results up to this point

Out of six YubiKey-supported services that I've looked at to this point (GitHub, Dropbox, Google, LastPass, Dashlane, KeePass2), I was only able to get the YubiKey to work with two services (GitHub and KeePass2). In both of these cases, YubiKey behaves a bit worse than I expected.

**Time spent so far:** I'm on the 23rd song on [Spotify's Brain Food playlist](https://play.spotify.com/user/spotify/playlist/67nMZWgcUxNa5uaiyLDR2x).

## Ubuntu login

First step:

```bash
sudo apt install libpam-yubico
```

Apparently, the Ubuntu login 2FA can work online and offline. Since I don't want to be locked out of my laptop when I'm not able to connect to WiFi, I've decided to try setting up the offline mode.

I did a `cat /usr/share/doc/libpam-yubico/README.Debian`, read everything and basically figured out that I'm looking at the wrong file and that I should be looking at the README file that is for some reason archived in `/usr/share/doc/libpam-yubico/README.gz` (it's the only file in that archive) to figure out how to set up the offline mode.

What I've discovered is that I need an API key. Okay, so I went to https://upgrade.yubico.com/getapikey/, typed in my email address, generated a one-time password by holding the YubiKey for three seconds, clicked on `Get API Key` and... god an "Invalid YubiKey OTP" message. Fuck.

Out of annoyance, I tried just tried tapping the YubiKey in the one-time password field. It worked! I got an API key! Yay!

Now, I needed to add a line to an appropriate file in `/etc/pam.d/`. How the hell am I supposed to know which of the 26 files in that directory is the appropriate one!? I'm clueless...

Back to Google (DuckDuckGo didn't show me anything useful).

I've found a tutorial named [How to configure Ubuntu 13.04 for use with A Yubikey](http://code.litomisky.com/2014/01/01/ubuntu-yubikey-2fa-config/). Unfortunately, I'm failing at the following step:

```bash
ykpamcfg -2 -v
```

...because:

```bash
Sending 63 bytes HMAC challenge to slot 2
Yubikey core error: timeout
```

Fuck this shit.

Let's try logging out and seeing if I screwed up anything. Wish me luck!

...

Ah! I didn't! Huh, that was a close one!

Yeah, at this point, I'm giving up on trying to set up a 2FA on my Ubuntu login screen.

I'm resuming the 34th song from the Spotify playlist and seeing what else can I try to set up with this thing.

Okay, since I'm logged out, I need to re-login into my KeePass2 database...

...

...generating one time passwords no longer works! It's possible that I forgot to save the changes I've made to the database. Fuck!

Back to having 1 working service properly set up with YubiKey. I guess I'll have to start all over and create a new KeePass database. Fuck. I'll deal with that later, I know how it goes now.

## PGP setup

Judging by [this page](https://developers.yubico.com/PGP/), I can set up YubiKey so I could use it with GnuPG, SSH and a bunch of other programs that I don't need to use it with. Let's try it with SSH!

I've executed [this bash script](https://github.com/dainnilsson/scripts/blob/master/base-install/gpg.sh). As the last line of output, I saw that I need to restart my laptop. Okay, minor annoyance, why not.

...

After restarting my laptop, I've tried ssh-ing into one of my company's servers. Successful. No 2FA.

But wait! The output of that bash script said something about autorunning some command, which I forgot to do. `gpg-agent --daemon` later... same thing. I'm logged in without 2FA.

Okay, maybe this is how it works. If I have a YubiKey plugged in, I get logged in. If not, I won't be able to log in. Let's try removing the YubiKey and ssh-ing again...

It worked... again... which means that my SSH setup didn't.

...

Five songs later, I went through other two tutorials applicable to Ubuntu ([Linux](https://www.esev.com/blog/post/2015-01-pgp-ssh-key-on-yubikey-neo) and [Another guide for Windows, OS X and Linux](https://jclement.ca/articles/2015/gpg-smartcard/)) and failed miserably to edit the key properly.

I'm getting really discouraged by now, plus I've managed to permanently lock my GPG card (I backed up the key before doing this, so no harm done... I think). I have to call it another failure. :(

## It's time for me to give up...

So, at this point, I've tried to set up YubiKey to work with the following:

* GitHub
* Google
* LastPass
* Dropbox
* KeePass2
* Ubuntu login
* PGP Setup / SSH connections

Out of all of these services, I was only able to set up YubiKey 2FA with GitHub and _partially_ with KeePass2 before I screwed something up.

**Time wasted:** 45 songs in a Spotify playlist. If the average song is 4 minutes in size (it's probably bigger, but let's go with the lower estimate), that's three hours on a Saturday completely wasted without actually gaining any extra security.

Now, yes, some of these fails are completely my fault: I refuse to switch to Google Chrome just so I could use YubiKey and I refused to pay for a LastPass Premium to be able to use YubiKey with it. But, in my defense, I did went through the hassle of trying to switch to a different password management solution to be able to use YubiKey. Unfortunately, I somehow managed to screw things up there too.

## YubiKey review

Services you can use it with are _very_ limited (I kind of expected way more supported services, like Twitter, Facebook, and other online services that support software-based 2FA). To be able to use it, you'll probably have to be prepared to change your browsing habits in some way, and you'll probably have to spend a considerable amount of time trying to set it up.

**Would I call these three hours time well spent?** Well, it was definitely fun to play around with it, but after every fail to set up some service, I got a little bit more discouraged. At the end, I feel really bad because I haven't gained any considerable improvement in my security.

**Is there something else I could try?** Definitely. I could try:

* "Cheating" Dropbox and Google setup by using Chrome's browser agent.
* Restoring my GPG key from the backup I made and see if I'll have a little bit more luck with it later when I'm a little bit more relaxed (by "a little bit more luck" what I really mean is "not locking my GPG card").
* Re-creating a KeePass database for the third time and importing my LastPass data for the third time into it and try really hard to _not_ log out / restart my laptop without hitting <kbd>Ctrl</kbd> + <kbd>S</kbd> and locking my database first.
* I could pay $12 per year for a premium LastPass account, but considering that I don't need a premium account for any other case, I don't think that this is a fair price to pay to be able to use a security tool that I have already paid.

I might try some of these things later, but now I'm too discouraged to try anything else.

I'm calling this a failure.

**Should you buy a YubiKey?** Depends on you. I don't think it'll become one of my essential tools. I think I'll just continue using Google Authenticator on my phone.
