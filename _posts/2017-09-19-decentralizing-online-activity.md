# Decentralizing my online activity one step at a time

I've started to become more restless about my online activities. I wanted to find a perfect sync between centralization and decentralization, and self-host my online life. So, how do I achieve this?

## 1. Sketching out what you actually do digitally.

In order to start this exercise, I first needed to understand what I actually _do_ online. And this could be tricky! Really tricky. You need to think deep, to map out all the things you do online, and to map out what could be decentralized and what could not.

> So, what are the things you can't live without?

The answer was... not that difficult. Here's a list of everything I wrote down:

**image 0**

As you can see, on the left, you can see a vague description of something I do on a regular basis. On the right, you can see the solution I used before starting this experiment.

Now, of course, some of these problems are impossible to decentralize (like, playing games), while others were already decentralized in my case (like, writing). However, there are some problems that could easily be ticked with a self-hosted solution:

**image 1**

Time for the next step.

## 2. Seeing what you already got

Before I could continue, I needed to answer a couple of questions:

1. What end devices do I already posses?
2. How difficult would it be to make them all work seamlessly?
3. What happens if I somehow lose one of them?

Before doing this exercise, surprisingly, I've never realized that I actually have _four_ end devices that I use on a regular basis! They are:

* **Laptop:** Lenovo Yoga 510 that is running Ubuntu GNOME.
* **E-ink display:** Kindle Paperwhite.
* **Smartphone:** Nexus 5x that is running Android Oreo.
* **Raspberry Pi** as a home media center.

## 3. Imagination time

What's the ideal situation in which I could be? How could I approach all of these things seamlessly? What are all those funky and cool solutions that I could develop?

Here's some of the things I came up with:

* Goodreads lists that automatically update Markdown files.
* My Calibre library needs to be on my phone, Kindle and my laptop.
* Photos I take with my phone should be available on my phone, on a server, on my external hard drive.
* Newest episodes of [Diplo & Friends](http://www.bbc.co.uk/programmes/b01dmw90) should be on my phone as soon as they are out.
* On my laptop, I should have a central point upon which I can access all of these different tasks.
* Ideally, in case one of my devices fails, no data would be lost.

## 2. Finding a server and creating a monster

Next step was to choose the platform upon which the rest of the decentralization will happen. In this situation, you kinda have to think of a solution that ticks most of your boxes. Are you interested in automating your home? [Home Assistant](https://home-assistant.io/) might be the perfect choice for you. Are you interested in purely developing code? Then [GitLab](https://about.gitlab.com/) might be the solution you're looking for. Are you interested in decentralizing your online life? Then Nexcloud is probably the way to go, and [Nextcloud](https://nextcloud.com/) is exactly what I went with.

Nextcloud's app ecosystem solves a lot of things I wanted to do out of the box. Bundling it with a couple of Nextcloud apps, and I got the following:

* Nextcloud -> replaces Google Drive / OneDrive / Dropbox.
* [Contacts](https://apps.nextcloud.com/apps/contacts) -> vCard / CardDAV replacement for Google Contacts.
* [Calendar](https://apps.nextcloud.com/apps/calendar) -> WebDAV replacement for Google Calendar.
* [Bookmarks](https://apps.nextcloud.com/apps/bookmarks) -> replacement for Pocket.
* [Tasks](https://apps.nextcloud.com/apps/tasks) -> replacement for Todoist / Trello.
* [News](https://apps.nextcloud.com/apps/news) -> replacement for Feedly.


## 3. Syncing with end devices

Next stop is to make some sense out of all of this and to transfer all of my data somehow.

Most of the services I was already using already offered some sort of the exporting options, and I was able to quickly switch between using a proprietary and self-hosted solutions.

Surprisingly, syncing all of this with my Android device turned out to be more challenging than syncing with GNOME. Syncing with GNOME simply consisted of adding my Nextcloud account in the Online Accounts settings and installing the Nextcloud desktop app.

Now, Android sync is a bit of a mess, and involves installing [DAVdroid](https://davdroid.bitfire.at/), [OpenTasks](https://github.com/dmfs/opentasks), and a whole lot of other things.

## 4. Password management

Since I don't like to keep my passwords on a server that I don't control, I had to find an alternative to LastPass, a service that I reluctantly used for a number of years.

KeePass / KeePassX / [KeeWeb](https://keeweb.info/) are all cool and stuff, but syncing between my laptop, my Nextcloud instance, and my phone with it is simply too complicated.

Luckily, I found out about [Enpass](https://www.enpass.io/). While their end apps are proprietary, the data gets stored on my device and it's up to me how I want to sync it. And, more importantly, it provides an OwnCloud / Nextcloud syncing mechanism out of the box, so I'm able to sync my passwords between my two end devices without any issues. If my server goes down, I still have two offline copies with the last sync.

The only price I had to pay is a one-time purchase of the pro version on the mobile phone.

**Total cost:** $9.99 one time purchase.

## 5. Note taking and code hosting

I am a big fan of GitLab, but until some sort of a syndication between the servers occurs, I don't see myself running an instance of it any time soon. I want most of my code to be public and reachable, and GitHub just does the trick as far as that is concerned.

So, I cash out $7 per month to be able to store as much code there as possible.

## 6. Following the news

## 8. Social networking issue

## 7. Bonus points

## 9. Front-end to my online life

* [ ] Data backup
* [ ] Bookmarking
* [ ] Keeping contacts
* [ ] IM solution
* [ ] Calendar scheduling
* [ ] Note taking
* [ ] Pw management
* [ ] writing
* [ ] sharing code
* [ ] commenting
* [ ] reaching out
* [ ] online persona ("front-end")
* [ ] sharing docs
