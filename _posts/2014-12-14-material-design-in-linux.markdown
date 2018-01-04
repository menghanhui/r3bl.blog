---
author: Aleksandar Todorović
comments: false
date: 2014-12-14 02:02:24+00:00
layout: post
slug: material-design-in-linux
title: Material Design in Linux
categories: en
tags:
- technology
image:
  feature: abstract-1-3
---

First of all, I do realize that I'm probably a few months late to talk about this topic. This topic is far from something new and something groundbreaking. Don't believe me? Well, this video from Google now has well over 2 million views.

http://www.youtube.com/watch?v=Q8TXgCzxEnw

So, what exactly is material design? Well, it's a [design language](https://en.wikipedia.org/wiki/Design_language) developed by Google. The whole point of this design language is that every graphical user interface should be as simple and colorful as possible. The point of that is, of course, to provide users with an interface which is pretty appealing to the eye.

Google already implemented material design in the newest version of Android called Lollipop. You can easily see the whole point of material design by looking at this excellent [Android 5.0 Lollipop Review](https://www.youtube.com/watch?v=cLYE3fgWI_4) done by [The Verge](http://www.theverge.com/) guys. The plan for Google is to implement this design language to every single one of their services.

Linux community embraced the whole material design idea pretty quickly. So, we already have this thing called [Quantum OS](http://quantum-os.github.io/) (previously known as Quartz OS). The point of this project is to create an operating system (which will probably be based on Arch Linux) that will follow Google's own [material design guidelines](http://www.google.com/design/spec/material-design/introduction.html).

I remember reading somewhere that it's not fair to the KDE community to say that they've implemented the material design because some of the KDE 5 mockups were out far before Google released the whole material design idea to the public. Anyway, KDE Plasma 5 does seem to fit the concept, as you can see by looking at one of the huge number of YouTube reviews if you search for [KDE Plasma 5](https://www.youtube.com/results?search_query=kde+plasma+5).

And now I came to the whole point of writing this post. I found out about a material design solution that I can implement right now using my current setup. As you may know already, I'm a huge [elementary OS](http://elementaryos.org/) fan. elementary uses Pantheon as a DE, which is based on GNOME and uses GTK.

So, today, [Sam Hewitt](http://snwh.org/) published the first GTK theme (at least that I know about) that was created with the goal of implementing the rules of material design. The theme is called [Paper](http://snwh.org/paper/) and it's in alpha stage at the moment. It looks wonderful and I'm pretty happy with how well the theme integrated with my elementary OS.

![Screenshot](http://snwh.org/paper/screenshot.png)

If you want to use it, all you need to do is to extract the folder called Paper in the tarball into your '/usr/share/themes' directory and that's it. If you experience some problems with the theme, [this](https://github.com/snwh/paper-gtk-theme/issues) is the proper place to report bugs.

I hope that Sam will continue to work successfully on such a great GTK theme and that we will see more of the material design GTK themes soon!
