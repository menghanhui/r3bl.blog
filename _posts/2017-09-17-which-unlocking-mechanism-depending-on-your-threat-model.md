---
author: Aleksandar Todorović
comments: false
date: 2017-09-16 11:30:00+01:00
layout: post
slug: how-to-unlock-your-phone-depending-on-your-threat-model
title: "Which unlocking mechanism you should use on your phone depending on who you're up against"
categories: en
tags:
- personal
- browsers
- Chrome
- Chromium
image:
  feature: abstract-1-3
---

Security-focused people usually follow the same rule of thumb on how you should unlock your phone: something you have to do is usually ranked higher than something you have to provide. I don't think I have ever consumed the content in which different scenarios are observed to confirm this rule of thumb, so this is my attempt at doing exactly that.

![random photo from the Internet](https://i.imgur.com/lBiWpQJ.jpg)

To do this, first let's define some threat models, rated from the most incompetent (and most likely to face) to the most competent (and most likely not to face):

1. [Generally incompetent thief](#generally-incompetent-thief)
2. [Generally competent thief in a passive attack](#generally-competent-thief-in-a-passive-attack)
3. Generally competent thief in an active attack
4. Police that doesn't care about ethics or mafia
5. Police that does care about ethics
6. Unlimited resources adversary that can't force you to do something

Second, let's define ways in which you can unlock your phone:

1. You have to do something:
  * Pattern (AKA connect the dots)
  * PIN
  * Password
  * Knock code (pressing specific areas on the touchscreen in a pre-defined sequence)
  * ...
2. You have to provide something:
  * Fingerprint
  * Face detection
  * ...

And now, let's compare how these two types of categories on how you should unlock your phone compare to each of the threat model.

## 1. Generally incompetent thief

Generally incompetent thief is the type of the thief that really doesn't know much about phones. He knows hardware is valuable, he doesn't give a crap about the data on the device. However, before he could re-sell the hardware, he's presumably gonna have to have access to the device or sell it cheaply.

As such, under the condition that the thief from this scenario only has one encounter with you, (almost) all of the unlocking mechanisms will protect you.

The only unlocking mechanism that could potentially fail in this scenario without your cooperation is face detection, because the thief would be able to flash the phone in front of your eyes before escaping.

**What will protect you without your cooperation:** Pattern, PIN, password, fingerprint, knock code.

**What could fail without your cooperation:** In an idealistic-for-me-as-an-adversary scenario, face detection.

## 2. Generally competent thief in a passive attack

**For those who don't know:** Passive attack is the attack in which nobody's targeting you specifically. You just happen to be at the wrong place at the wrong time.

In the generally competent thief scenarios (so, this one and the next one), I'm gonna make myself as an adversary and give myself a reasonable amount of resources (let's say up to $10k). Presumably, my goal would also be to make sure I can't get caught.

**NOTE:** In this scenario and the next one, I am not saying that I'm super smart, I am just interested in security and like to imagine things.

If I notice you using fingerprint or face detection, and if I don't think you're valuable enough to get to your data, this is the moment in which I would give up and look for another target. I need a close encounter with you to obtain any of those, and the hardware itself is simply not worth the risk (even if your phone costs $999).

If I see you using any other unlocking mechanism (PIN, pattern, password, knock code), and you happen to be in an area that I have under video surveillance, I would make an attempt to steal your phone only after I have video evidence of you unlocking your phone (so that I could duplicate it). In this scenario, passive attacks could be done just by me having access to the security cameras in a place where people spend some time (cafes, restaurants etc.).

**What will protect you:** Fingerprint and face detection.

**What will not protect you:** The unlocking mechanisms in which you have to do something, provided that you're at the wrong place at the wrong time.

## 3. Generally competent thief in an active attack

**For those who don't know:** As you might imagine after reading about what a passive attack is, an active attack is an attack in which you specifically are being targeted.

The simplest way in which I can make this happen is by hiring someone else to do it for me, someone who is willing to physically threaten you up to a point where you are scared enough to give away anything you need to the person I've hired.

In the situation where you're unlocking your phone with something you know, chances are high that you're gonna use something convenient (a simple pattern) and that the person I've hired will be able to memorize it.

On the other hand, something you need to provide is a bit trickier, because the person I've hired will need to make you cooperative for long enough time to make you turn this method off.

**What will protect you in an active attack scenario:** In an idealistic-for-me-as-an-adversary scenario, nothing. If the scenario doesn't turn out to be idealistic for me, something you have to provide has a higher chance of succeeding than something you have to do.

## 4. Police that doesn't care about ethics or mafia

I am bundling police that doesn't care about ethics and mafia in the same scenario, because both of them don't simply care about possible consequences.

This explanation is rather short, because it is easily summarized by the famous Security XKCD:

![xkcd security](https://imgs.xkcd.com/comics/security.png)

**What will protect you in this scenario:** Nothing.

## 5. Police that does care about ethics

If the police does care about ethics, they would probably require a court order to make you unlock your phone. However, face detection could fail if they have some way of tricking you into looking at your phone, and that wouldn't be unethical _per se_ because they're not forcing you into doing anything.

**What works in this scenario:** Everything except face detection.

**What fails in this scenario:** Under the condition that they don't have a court order that forces you to unlock your phone, face detection is the only thing that could possibly fail.

## 6. State-sponsored adversary that can't force you to do something

Fingerprints and face detection can all easily be faked with unlimited resources.

As far as the public is aware, in situations where you have to provide something, the timeout after a couple of false attempts is enough to stop state-sponsored adversary from directly unlocking your phone. There are probably other ways that they could think (not updated Android might have some CVE that they could use, and in the worst case scenario, they might have a zero day that will work, but that's out of scope of this scenario).

**What fails:** Fingerprint and face detection.

**What works:** Something you have to do.

## Conclusions

From these six scenarios, I reach the following conclusions:

* Something you have to do (PIN, pattern, password, knock code) will stop the advanced attackers in every scenario in which they can't observe you nor threaten you.
* Something you have to do will fail if the attacker is in an opportunity to observe you long enough or threatens you.
* No two methods are the same, but for 9X% of the world population, something you have to provide is good enough.
* Within the current choice of something you have to provide methods, fingerprint detection beats the hell out of face detection in every single scenario, since fingerprints are more difficult to obtain than your face (which is the most public thing you have).
* Fingerprint detection is good enough in lower threat model situations, and from now on, I will recommend it to everyone who doesn't work in tricky situations.

This last conclusion kind of bums me out, since the security-focused people were basically all against it once it started rolling out. In fact, once I've started writing this article, I was _convinced_ that fingerprint scanners will fail this test. Turns out, I was wrong.

_P.S. If there's something wrong with any of my situation assessments, please contact me on [aleksandar@r3bl.me](mailto:aleksandar@r3bl.me) or comment on the other platforms where this article gets shared. I'm turning off the comments on this article to prevent people who haven't put a reasonable amount of effort in consuming my arguments from commenting on my conclusions._
