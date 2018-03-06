---
title: Three ways of re-creating Firefox Focus behavior on Firefox desktop
date: 2017-10-20 04:00:00 +02:00
categories:
- en
author: Aleksandar Todorović
comments: false
layout: post
tags:
- advocacy
- tutorial
- technology
- browsers
- mozilla
- firefox
- ux
---

Before I've started experimenting with re-creating Firefox Focus on the desktop, I thought that a browser like Firefox Focus for the desktop could be a huge win. Now, I realize that replicating its key features in a well-known browser is a relatively simple thing to do.

![Firefox Focus hero image]({{ site.url }}/images/mozilla/focus-hero.png)

For those of you who don't know, [Firefox Focus](https://www.mozilla.org/en-US/firefox/focus/) is a mobile-only web browser that deletes your session on a tap of a button and offers tracking protection out of the box. In this article, I'm gonna explain how to recreate this behavior on the desktop version of Firefox.

Before I go any further, I wanna quickly summarize my workflow on my mobile phone:

> Firefox Focus is set as my default browser, so all the links I click automatically open in it. However, it is not my primary browser, as I have another one used specifically for the services where I want to remain signed into.

...and I wanna add a small note:

> These scenarios were explored on Ubuntu, and storage locations mentioned here together with some commands are Ubuntu-specific. However, with a bit of searching around, all of this is accomplishable on all desktop platforms.

Now, let's set the objective to match the two key features of Firefox Focus:

1. Blocks a wide range of common Web trackers.
2. Easily erases your history — no passwords, no cookies, no trackers.

## Option 1: Out-of-the-box solution in a couple of clicks

To re-create both of the key features on an out-of-the-box Firefox desktop installation, you just need to change two things:

1. Go to "Menu" -> "Customize" and drag the Forget button somewhere where it's easily reachable.
2. Go to "Menu" -> "Preferences" -> "Privacy & Security" -> under the History section, select "Use custom settings for history" -> tick the "Always use private browsing mode" checkbox.

Since Disconnect.me's lists are used both in the private browsing mode ([source](https://support.mozilla.org/en-US/kb/tracking-protection-pbm#w_block-lists-in-firefox)) and in the Firefox Focus browser ([source](https://github.com/mozilla-mobile/focus-android/wiki/Content-blocking#the-blacklist)), you'll achieve pretty much the same result.

On top of that, "Forget" button allows you to quickly delete everything and start from scratch (equivalent to the Erase button in Firefox Focus).

The **caveat** here is that the Forget button deletes your activity from the specific amount of time, and the maximum you can select is 24 hours. So, in case you don't press the Forget button for over 24 hours, you will need to re-start Firefox in order to truly start from scratch.

That's pretty much it. To solve my use case, all I need to do is to use a different browser for the things where I want to remain signed in, and have Firefox set as my default browser.

This option is for you if you fall under one of these categories:

* You want _all_ your browsing sessions to be temporary.
* You're comfortable with using a non-Mozilla browser for the permanent session.

This option is not for you if you wanna remain signed into some services and wanna remain using Mozilla's browser exclusively.

Since this option is not for me, I went ahead and searched for other ways to accomplish the same thing.

## Option 2: Different Firefox profiles/versions + option 1

If you wanna remain in the Mozilla ecosystem and still achieve the things we've achieved in the first option, you're either gonna need different profiles (one default one, one with a Focus-like behavior) or two different Firefox versions installed at the same time.

**What are Firefox profiles:** Firefox profiles are local sets of profiles that you can switch between. Creating a new profile creates a new subdirectory in `~/.mozilla/firefox` where the new settings get stored. Profiles feature is local-by-default, with an option to use Sync if desired.

Firefox profiles feature is tucked away. There is no GUI-only way to reach the profile manager as far as I can tell, so you're gonna have to follow these instructions:

1. To open the profile manager feature, close Firefox and start it again from the terminal using `firefox -ProfileManager`.
2. Create a new profile and give it a name (like Firefox Focus).
3. Un-tick the "Use the selected profile without asking at startup" option.
4. Click on "Start Firefox".
5. Follow the two steps explained in the option 1 to re-create Focus-like experience.

![Firefox profile manager layout](https://i.imgur.com/4VAGmcr.png)

Now you can start two instances of the browser by starting Firefox however you usually start it (which will start Firefox with the default profile) and then running `firefox -p "Firefox Focus" -no-remote` (where `-no-remote` tells Firefox to start an entirely new process).

To streamline this a bit, you could do something like `cp /usr/share/applications/firefox.desktop ~/.local/share/applications/firefox-focus.desktop`. Then, modify the `firefox-focus.desktop` file (I wouldn't recommend doing it the other way around because `firefox.desktop` will probably get overwritten when you upgrade to a new Firefox version). The bare minimum version of the `firefox-focus.desktop` file would look like this:

{% highlight ansired %}
[Desktop Entry]
Version=1.0
Name=Firefox Focus
Comment=Browse the Web privately
GenericName=Focus Web Browser
Keywords=Focus;Internet;WWW;Browser;Web;Explorer
Exec=firefox -p "Firefox Focus" -no-remote %u
Terminal=false
X-MultipleArgs=false
Type=Application
Icon=firefox-focus
Categories=GNOME;GTK;Network;WebBrowser;
MimeType=text/html;text/xml;application/xhtml+xml;application/xml;application/rss+xml;application/rdf+xml;image/gif;image/jpeg;image/png;x-scheme-handler/http;x-scheme-handler/https;x-scheme-handler/ftp;x-scheme-handler/chrome;video/webm;application/x-xpinstall;
StartupNotify=true
{% endhighlight %}

Then, download the Firefox Focus icon (you can do that [here](https://github.com/FirefoxUX/product-identity/tree/master/images/firefox-focus) or [here](http://design.firefox.com/photon/visuals/product-identity-assets.html#firefox-focus)), place it in `~/.local/share/icons` and you're done.

Two important **caveats**:

1. You can't open Focus first, and then Firefox. You'll receive a "Firefox is already running" message. This could be changed by adding `-no-remote` flag to `firefox.desktop` on all three lines that start with `Exec=`.
2. Side-by-side, they look like this:

![Screenshot from 2017-10-20 03-17-47.png](https://i.imgur.com/1x4qgtK.png)

You can notice that the left one is the default one because I did some slight interface modifications. However, that's not big enough of a distinction for me to tell on the spot if I'm running the Focus version or the default one. So, as a final step, I would recommend installing a custom theme (like [MozillaFocus](https://addons.mozilla.org/en-US/firefox/addon/mozilafocus/)) to make the distinction a bit more obvious:

![Screenshot from 2017-10-20 03-21-55.png](https://i.imgur.com/NOjRLRS.png)

Much better!

If you're too lazy to edit the `.desktop` files manually and play with the profile manager, an easier way to accomplish the same result would be to install either a stable + nightly version of Firefox, or beta + nightly versions. Stable + beta is not easily achievable because the beta PPA upgrades the `firefox` package, unlike the nightly PPA which installs a brand-new `firefox-trunk` package.

Simply set up one of the versions as described in option 1. Remember that Firefox is your permanent session browser and Nightly is your Focus-like experience (or _vice versa_) and you're good to go.

This second option should suit almost everyone. The third option is there if you don't like having multiple browser windows open at the same time.

## Option 3: (Experimental) Container implementation in the same browser window

**DANGER:** While this option _does_ delete cookies and other session data, it _does not_ delete the websites from your browsing history. The browsing history is currently not being split into containers. According to Mozilla's wiki, this [is a planned feature](https://wiki.mozilla.org/Security/Contextual_Identity_Project/Containers#What_is_.28and_isn.27t.29_separated_between_Containers).

Final option I'm going to mention is the one in which you're gonna be using the same browser window and the same Firefox version. In short, we're gonna use the [contextualIdentities API](https://developer.mozilla.org/en-US/Add-ons/WebExtensions/API/contextualIdentities) (which is also used in the Mozilla's own [Firefox Multi-Account Containers](https://addons.mozilla.org/en-US/firefox/addon/multi-account-containers/) add-on). While the Mozilla's add-on separates your browsing into different identities, there are other add-ons using the same API a bit differently.

The add-on that is a crucial part of this experience is called [Containers On The Go](https://addons.mozilla.org/en-US/firefox/addon/containers-on-the-go/). To put its behavior in a simple context: once you start a container, you start a new session. Once you delete a container, the session and the data from it gets destroyed. So, what this extension does is it allows you to start a new session by dynamically creating new containers, and then automatically destroys them as soon as you close all the tabs the created containers.

If you decide to use this extension, you can create a new container in three different ways:

* By triggering the <kbd>Alt</kbd> + <kbd>C</kbd> keyboard shortcut.
* By clicking on the extension icon in the tab bar.
* By right-clicking on a link and choosing "Open link in new container".

Unfortunately, you can't have different settings for different containers (like you can do by using different Firefox profiles), so you're gonna have to have some sort of tracking protection installed globally. You also won't be able to use the built-in "Always use private browsing mode" option, since that option will automatically close the sessions you want to keep as well. Therefore, you're gonna have to rely on a third-party tracking protection add-on.

Screenshot of the add-on in use:

![Screenshot from 2017-10-20 04-06-35.png](https://i.imgur.com/gcAHeed.png)

In this screenshot, I'm signed in in the first two tabs (so, Hacker News and GitHub), while the other four tabs are in their own separate containers. These four tabs don't have access to my cookies from the default session and they don't have access to the cookies from each other's sessions. As soon as I close any of these tabs, everything related to it gets destroyed automatically.

And, finally, I've found an implementation that I really like. While the second option with two different Firefox profiles might be a bit more complete of a solution, this one is simply one add-on install away.

---

**Worth pointing out:** While I am directly tied to Mozilla as a Ford-Mozilla Open Web Fellow, I am not a part of the Firefox team, just a happy user.
