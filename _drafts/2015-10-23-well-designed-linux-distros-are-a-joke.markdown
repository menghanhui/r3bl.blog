# Designers, please stop designing your own Linux distros

Seriously, stop. It's getting us nowhere.

First of all, I want to say that my Linux journey has not been that long. I've been a Linux user for ~3 years now. When I started, I played around with different distros until I found [elementary OS](https://elementary.io/). It has its own desktop environment (called Pantheon) which, at the time, was light enough not to cause major issues with my hardware setup (note that [this issue](https://bugs.freedesktop.org/show_bug.cgi?id=73338) was resolved around April this year), it looked sexy, the system was based on the LTS version of Ubuntu... it was just perfect for me (and still is).

elementary OS is still a relatively young distro. The current version is 0.3.1 (codenamed Freya). This is the first distro (that I know of, I'm probably wrong) that was made to be sexy by design. It gained its popularity quite quickly and it is now probably one of the most popular desktop solutions out there (although, there's no real way of testing this out, Daniel Fore (AKA elementary's main developer) does a good job of explaining its popularity [in a reddit comment](https://np.reddit.com/r/linux/comments/3uajcs/is_elementaryos_falling_out_of_favor/cxdgwlv)).

Now, let us examine the path elementary's team took:

1. Create an icon pack and a Gtk theme.
2. Fork GNOME and make it look a bit better (0.1 version).
3. Create your own desktop environment and start making native apps that fit to the overall design of the OS (0.2 version).
4. Instead of doing major design changes, focus on the small things and make your default apps usable (0.3 version).
5. Register your project as a LLC (Limited Liability Company), receive donations on a monthly basis and start employing people.
6. Who knows?

I have started using elementary OS while it was in its third step on this path. I never actually stopped. It quickly became my go-to operating system. Now it's the only operating system I'm using. I don't know what elementary OS was like during its initial (0.1) version and I don't know the exact reason why the developers decided to make its own operating system, but they made it work. It gained traction, it has its own user base (thousands of people in its [Google+ community](https://plus.google.com/communities/104613975513761463450)), it has its own [Q&A system on StackExchange](http://elementaryos.stackexchange.com/) (currently in public beta), it receives commits on an (almost) daily basis (quote from Daniel's reddit comment I linked to earlier), it started actually employing people and stopped being a side project of a few, its team contributes back to other open source project... It has everything needed to grow even further and I have no doubts that it absolutely will.

Saying all of this without mentioning any of the hiccups they had during their path would be a bit wrong (or make me look like a fanboy that's only bashing on other people's projects), so I'm going to list some of the problems they are (or were) facing:

* In one of their blog posts, they called the users who download their operating system without making a donation cheaters. While they had apologized and the person who made that post said that this was simply a bad choice of words, this action did leave a bitter taste in people's mouths at the time (especially in /r/Linux where this keeps being mentioned even now, over a year after that it happened).
* It currently uses Canonical's Launchpad for the development. I think of this as a problem because Launchpad's design is heavily outdated. Sure, it makes the development of a Ubuntu-based distro easier, but its UX is much worse than GitHub's (or Gitly's). It kind of feels wrong using such an outdated tool (I'm talking about its design) to make a project that focuses on looking good.
* Some of their default apps still need some fine tuning. There are still bugs to squash, functionalities to be added and dialog boxes that should be simplified.

While using elementary OS, I became interested in similar open source projects that focus on the design first. And boy, did the elementary OS inspire _a lot_ of people! Since I've started using elementary OS, I learned about a dozen of other Linux distros that basically want to do the same thing: make a Linux-based operating system that looks good. However, I think that the people who are behind them are completely underestimating the amount of work needed to create, maintain, and further develop an operating system. Let's take a look at these projects one by one (in the alphabetical order):

## Apricity OS

> Welcome to Apricity OS, a modern, intuitive operating system for the cloud generation of computing. We believe that an operating system should be easy to use, easily accessible, and beautifully designed. We have also incorporated software in order to minimize security risk as much as possible.

![ApricityOS](https://camo.githubusercontent.com/cd3dc47ad7b849813b535194f7eacbf73c7f5e32/687474703a2f2f61707269636974796f732e636f6d2f6173736574732f696d672f6261636b2f61707269636974792d6c6170746f702e6a7067)

[Apricity OS](https://apricityos.com/) seems like nothing more than a stripped down version of GNOME bundled with a couple of third-party applications installed by default (the full list of preinstalled apps is located [here](https://github.com/agajews/ApricityOS/blob/master/apps.md)). Its documentation consists of long chunks of texts packed into a single paragraph for no apparent reason (see the example below). The "security features" consist of nothing more than using UFW and some backup software. I really don't see any reason to create this operating system. It seems like the whole job is being done by a single person who knows how to create an OS installer. Nothing more, nothing less.

![Apricity OS installation instructions](http://i.imgur.com/6iRENQC.png)

## Ozon OS

[Ozon OS](http://ozonos.github.io/) was the Linux distro I was hoping for the most. The idea was to unite the forces of [Numix](https://numixproject.org/) and [Nitrux](http://nitrux.in/) projects, both of which are well known for creating good looking Gtk themes and icon packs. Unfortunately, the idea never came to life as the team decided to shut the project down and merge their forces with the [Korora project](https://kororaproject.org/) before they released their first stable version.

![Ozon OS Hydrogen Beta](http://3.bp.blogspot.com/-ql_NSQUn6jI/VP7vvF2dPII/AAAAAAAAVzU/_gto2E0SUgY/s1600/ozonos-beta.png)

Ozon OS is not the only project that got shut down early in the development process. I will mention quite a number of them at the end.

## Papyros

When Ozon OS got shut down, [Papyros](http://papyros.io/) became the distribution I was looking forward to the most. Based on Arch, it promises to bring material design to Linux. Unfortunately, I have never actually tried it out since I'm too lazy to install Arch with Papyros on top of it, but their 0.1 version is ~90% done, so I'm assuming it won't take long before I try it out. In the meantime, I can only feast my eyes on the preview image:

![Papyros](http://papyros.io/images/papyros-laptop.png)

## Solus

I would love to quote a single paragraph that explains what Solus is, but that doesn't seem possible.

## The long list of dead projects

* (Previously mentioned) [Ozon OS](http://ozonos.github.io/) - I have already stated everything you need to know about this project that died pretty quickly.
* Evolve OS - This is essentially Solus before it got completely renamed to Solus.
* 

## Why we don't need any more Linux distributions

Don't get me wrong, I love to see a well designed Linux distro, but this seems like it's getting out of control. With so many teams leading their Linux distributions in so many different directions, while focusing in one goal that's essentially the same, it's immensely hard to make a good product.

I am well aware of all of the advantages of the open source software. Being able to fork something is just one of them. _But_, creating a Linux distribution is a _huge_ development effort that cannot be accomplished so easily. Designers seem to regularly undermine the amount of work needed.

So, instead of making more Linux distributions, my suggestion to everyone interested in making Linux look prettier is to get involved with some of the projects that are already out there.
