---
author: Aleksandar Todorović
comments: true
date: 2015-08-22 15:17:00+01:00
layout: post
slug: on-open-source-donations
title: "On open source donations (from my perspective)"
categories: en
tags:
- rant
- open source
- Linux
image:
  feature: abstract-1-3
---

It's no secret. If you have a large multi-million company financing you, your open source project will be successful. You can hire people to work on your open source projects and I bet you could make something that will catch people's attention.

But what if you don't have that kind of a company pushing you forward? After all, you're not really selling your software, so how can you make a living by making it? The ideal solution would be to make an open source project that's going to be used by thousands of people out of which at least a hundred would be willing to donate like 10 dollars per month to support it, but seems like that never turns out to be the case.

## Bullshit excuse number 1

> You're just building your software upon somebody else's project. Why should I donate my money to you?

First excuse that pops in my mind is that you're not building your project from scratch. If you're not building your project from scratch, why should the users donate money to you? Why not just donate to the project that you're based on? This is a bullshit excuse and here's why:

1. The project X is asking for money. The project X is an open source project based on the project Y. As long as the developers are not breaking the license of the project Y they're basing their project X on, it's fine. The beauty of open source is that you don't have to build your project from scratch. You can re-use the code written by somebody else. That's one of the points of open source licenses.
2. It's not like the developers of the project X will make a shit ton of money. If they had like a million dollars lying around, they wouldn't ask for more money, would they? Of course, there could be exceptions to this, but can you think of any exception? Because I certanly can't.
3. If the project X becomes big, you can bet that the developers of that project will find some way to contribute back to the project Y. They'll find a bug that wouldn't be usually found. They'll find some code in Y that executes rather slowly on a large scale and instead of coming up with a hack to make it work, they'll see the code that's bugging them, come up with a solution to that problem and submit a pull request to the project Y.
4. If they have some extra cash, they will give it to the project Y. It's in their interest to make the project Y better so their project X gets better too. They're aware that they wouldn't be able to make any money without project Y.

## Bullshit excuse number 2

> It's free software, I don't have to pay shit.

Free software is free as in freedom, but it's not free as in beer. In most of the cases, it's free (as in beer) _for the consumers_, but it's not for the developers. They still have to pay for their living, their equipment and they have to enjoy from time to time god damn it. They can't work on a project 16 hours per day every day. Nobody can. I'm just a 20yo, I don't have a wife and family, but the chances are small that I'm going to make something big. Something big is going to be made by someone with a lot of experience. Someone who knows what open source world needs. That person is probably going to already have a family that he needs to support.

Sure, he can have a regular nine to five job, support his family and work on a project for like two hours per day. That works fine once your project is small, but when its popularity starts to go up, so does the responsibility. Suddenly, two hours per day is not enough and we get stuck in a loop. If he can't work on a project regularly, he can't keep up with the demands of thousands of users. If he can't keep up with the demands, his project is not going to stay relevant. If his project doesn't stay relevant, his project starts to lose its user base who will eventually come up with some other competitive project Z. That other project is going to be small in the beginning, but as his popularity increases, he's going to face the same problem as the developer of now dead project X and we start to spin around in circles.

## Bullshit excuse number 3

> I would support them if they made this specific feature I need.

And how is he going to build it? In an ideal world, the developers will work on whatever feature its users are demanding the most. In real world, more features means more bugs. More bugs means more time is needed to squash them. With a limited amount of developers and resources, it's impossible to satisfy everything users are suggesting. Of course, there's absolutely no guarantee that if you donate something to the developers, they will build a feature that you suggested. You're just suggesting it. Other people suggested ideas before you. The developers already have a list of priorities in their head. Your suggestion might be the last one on their list.

If a feature A is wanted by 50 guys and those 50 guys donated $100 in total, but the project first needs to support the feature B so their project can support project A, they'll focus their attention on the feature B first. Then, if the feature B took too much time, the chances are, out of those 50 people, 25 people don't need the feature A anymore and now they want the feature C and so does other 35 people. But to implement feature C, they need to deal with feature D first. Suddenly, feature A goes down on the list, but the project is moving forward as it already implemented features B and D.

## Bullshit excuse number 4

> The team is not very approachable, so I don't believe them.

Okay, you like some sort of open source project. You would love to talk to a guy who made it, but you can't seem to get in touch with him and talk to him about his project. Well guess what! I bet there's 49 more people who want to talk to him for a longer period of time than you do. So, 50 people wants to talk to that developer. If the average conversation lasts for 30 minutes, that's 25 hours of his time that he could have spent programming.

Now, if you're going to say that he could talk to you after he's finished with everything he planned on doing today, well guess what! If you just spend 10 hours getting something to work and after those 10 hours you _still_ have a bug in your code that you just can't get rid of, are you going to feel like talking to me about that project? No, you will be frustrated, you'll call it a day, watch your favorite TV show, go out with your friends... basically, do anything not related to your project in any way so you can take your mind of that bug and relax a bit.

If the day went as planned, then he slept 8 hours and worked 10 hours which leaves him with 6 free hours. If he relaxed, ate, bathed and everything else normal people do in a day lasted for three out of those 6 hours, that leaves him with 3 hours to talk to those who want to talk to him about his project. If the average conversation lasts 30 minutes and he's really on a roll making good code a day after day, that means he will have time to talk you in like nine days.

## What the developers seem to forget

Now I'm not going to say that every problem with donating is user's fault. Developers seem to have a hard time figuring some things out too.

First of all, most of the open source projects are maintained in a highly technologically developed country (or at least I presume that's the case). A large chunk of your users are probably not living in a highly developed country.

A certain amount of your users might be mostly still using cash and don't have a credit card that's supported worldwide. As an example, I own a Maestro credit card. It satisfies most of my needs in my country and it's pretty popular in Europe, but it's not available in the U.S. As a consequence, I can't really buy a lot of things online. Same thing goes with donations. I have yet to find a single donation service that supports it.

120 dollars might not seem a lot for you, but it's enough for me to provide myself food and a bit of luxury for the entire month. The cost of living depends on where you live. Sure, I could probably donate 20 dollars per month to open source projects, but I have to carefully choose which open source projects should I donate to. If I choose four different open source projects and donate to each of them 5 dollars per month, that's not going to make a big difference to you, but it is going to make a difference on my budget. Here, where I live, I can buy a lot of things with 20 dollars.

Now, lets sum it up. If your project has 20 thousand users, lets say that one in eight people is interested in supporting your project. That leaves us with 2.5k users. Out of those 2.5k, one thousand of those can't support you financially regardless of their interest, which leaves us with 1.5k. If 500 is unable to support you for some other reason (like, their credit card is not accepted by the donating service you're using), that leaves us with 1k people. If 1k people donates 10 dollars every month, that's 10k dollars of income on a monthly basis, which is enough to pay like 10 developers. So, we end up with 10 developers who are financially able to support 20k users. And this is a highly generous estimate.

Also, there's a large number of people who are interested in supporting your project in some other way. They might be interested in writing code, spreading the word, answering questions to other users, providing translations, making suggestions, writing documentations, reporting bugs, replicating reported bugs and confirming them etc.

It's no secret that writing code is currently the thing that gets the highest amount of recognition in an open source community. But aren't other jobs equally important? Do those interested in becoming contributors in any of those ways feel welcome?

Code is important at first, but as the project gets more popular, other types of contributions become equally as important. So, stop bullshiting yourselves that you only have 10 contributors. In reality, I bet you have at least 50 people who are making an impact on your project even if only 10 of them ever made a pull request.

## What the users seem to forget

Open source projects are made by people. People like you and me. People who have 24 hours per day. People who can't _possibly_ be productive for more than 10 hours every day. And the number of people making code changes is not big. In reality, it's rather small and probably doesn't include more than 25 people who contribute code regularly. Out of those 25 people, 10 can work on a project only a couple of hours per week, 10 can work for like an hour or two every day, and _maybe_ five can commit their full attention to this project. There are people genuinely interested in making an impact on the project, but they just can't do it. They have jobs. They have family and friends. They can't quit their jobs because they can't be sure that they will be financially stable if they devote their full attention to the project.

In an open source ecosystem, you can't possibly give back as much as you are actually getting. If you're using _any_ Linux-based operating system, you're relying on work done by dozens, if not even _hundreds_ of people every single day. Chances are big that you haven't payed a dime to get _any_ of the software you're currently using installed on your system. If you have some spare time, donate your time. If you have some extra money, then at least buy the developers a cup of coffee.

In a proprietary ecosystem, a program or a web service is a product and you are the consumer. If you're getting something for free, you're the product. In an open source ecosystem, you're a part of the community whether you like it or not. 80% of the community doesn't do shit to support the community. Yes, they _are_ free and they _have_ the option not to get involved with an open source project, but that doesn't mean that you should not at least _consider_ being a part of the project. Being a part of the open source project will benefit every single one of its _and_ its developers.

In reality, far less than 20% of the users of open source projects are actually giving something back. That small percentage that _does_ give something back supports open source without a financial stability. 
