---
author: Aleksandar Todorović
comments: true
date: 2014-12-04 19:56:24+00:00
layout: post
slug: witcher-2-installation-from-hell
title: 'Gaming on Linux Is Still Not Very Noob-Friendly (Witcher 2: Installation From
  Hell)'
categories: en
tags:
- humoristic
- personal
- floss problems
- linux
- gaming
image:
  feature: abstract-1-3
---

Today I learned that gaming on Linux is still not very noob friendly. For a long while now I was looking for a first game to buy in my life. I've decided for Wither 2: Assassins of Kings. The game costs somewhere near $20 on [GOG](http://www.gog.com/) and I got the 60% discount deal so the game cost me $7.99 total.




The game itself is big, and I mean _really _big. I needed to download over 19 gigabytes, but what the heck, I bought it because I wanted to play it, so I went ahead and started the download. On the first try, download failed after 3,5 GB with no apparent reason. My internet connection did not break or anything like that. I felt discouraged but I wanted to give it another go, so I started to download the game, _again_. This time, I downloaded more than 7 GB of data and the download crashed again for no apparent reason.




There is no official GOG's Linux download manager for now, but after some searching around I did manage to find the unofficial one called [lgogdownloader](https://github.com/Sude-/lgogdownloader/) (thank you GitHub!). So I went ahead and installed it. It's a fine command line tool and it's not really hard to figure it out. After spending a half an hour connecting it with my GOG account (don't blame the developer of this tool, the fault is all mine) the time has come for me to try to download the game for the third time now.




This time, download was successfully finished and I had the game on my hard drive. Wow, finally, looks like I'm going to be able to play it! So after I extracted the whole 19 gigs of compressed data to a folder I felt very excited. Now all I had to do is to start the game and I'll be able to play it, right?




Well, of course not.




I know what is a launcher file, so I thought that all I needed to do is to give execution privileges to that file and the game should start, right? Well, no, the launcher didn't start because of some broken dependency. Thanks to the Ubuntu's huge repository, installing the dependency was not that big of a deal, just a standard _apt-get install_ command. After that I will finally start the game and that would be it.




**Aaaand finally, the launcher started without any errors in the terminal!**




Now all I needed to do is to click on Launch Ga... WHAT??? Broken dependency, again? Oh what the hell, _sudo apt-get install libsdl2-2.0_ should do the trick, right? All done, it's time to _finally_ start the game, right?




WHAT??? The same error _again_? But I _have_ installed _libsdl2-__2.0_! Back to Firefox and search for the issue. Oh, so I installed the 64-bit version of the package but I need the 32-bit version to start the game? Sure, no problem, repeating the last command with _:i386 _in the end should do the trick. Start the game again, aaand get a broken dependency error again!




So looks like I need one more package? OK, this time I won't repeat the same error, I'll install the 32-bit version right away. Now I have to admit that after going through such trouble, I do feel kind of frustrated and I just want to play the damn game. My inner hacker is exhausted so he took a nap and woke up 50-year-old grudged man inside of me from the couch. Let's see if he can finish the installation.




Of course, GOG laughs at my face and gives me another broken dependency. This time it's a package called _openal_. Sure, no problem, _sudo apt-get install openal_. What, not in the repository? Let's try to Google that. So I did manage to find the renamed package. Looks like it's called _libopenal0a_, so let's install it. _sudo apt-get install libopenal0a_. Wait, no release candidate? Let's Google some more. And while I'm searching for the solution, let's look at GOG's support, might want to contact them if something goes wrong.




So, the officially supported distros are Ubuntu and Linux Mint. Oh, crap, I'm not using _them_, I'm using [elementary OS](http://elementaryos.org/)! I don't think that the support will be willing to help me out, but they do have _some_ articles posted in their support section and elementary _is _built on top of Ubuntu 14.04, so I might check out those articles while I'm already at the support section.




Question: _How do I start the game I unpacked from a tarball (*.tar.gz)?
_Solution: _Run ./start.sh_




Oh, wait a second, I don't have any shell scripts inside my Witcher folder, but I do have the launcher, which is practically the same, right?




Question: _Why do you list required libraries on the game's product card?
_Solution: _… We'll always make sure to include a list of any potentially missing libraries that make up a game's minimum system requirements._




Thank you GOG! So all I have to do is to find minimum system requirements and I'll find the list of all packages I need to install and then I'll be able to run the game! I remember I saw a file called _readme_EN.rtf_ inside of my Witcher folder. So I opened it up and navigated to system requirements section.




What??? Linux is not even on this list??? Only requirements for Windows? What the hell? Back to Google-ing. Oh, marvelous! [Webupd8's article](http://www.webupd8.org/2014/05/the-witcher-2-assassins-of-kings-game.html) about the game release for Linux does contain the system requirements section. Now let's look for that list of packages I need. WAIT WHAT??? THE GAME ONLY SUPPORTS NVIDIA GPUs??? WHY IS THAT INFO NOT SHARED ON GOG's SITE???




Oh, it is. Crap.




...




OK, calm down.




_cd ..
rm -r the_witcher_2_




Note to myself: Next time, buy the damn game on Steam.




**DISCLAIMER:** I love GOG, this text is not an attack on them in any way. This is just a satire text to show you my stupidity.
