---
author: Aleksandar Todorović
comments: false
date: 2014-08-03 13:18:43+00:00
layout: post
slug: sensitive-data-grabber-project
title: Sensitive Data Grabber Project
categories: en
tags:
- technology
image:
  feature: abstract-1-3
---

So, what I want to present to you today is a project I'm currently working on. What I'm doing is I'm creating a program that will collect all of the sensitive data from the victim's computer and saves them on a thumb drive. The program is currently being written as a form application using Microsoft's Visual Basic and .NET framework 4.5. After I finish the beta version, I'm planning on re-writing the program so it will be a console application and it will work with some older .NET framework (I'm not yet sure which .NET framework will I support for now).

Now, what I want to do is to tell you what this program actually does for now and what I'm planning on implementing.

First of all, the program will collect some basic data about victim's computer. That data includes information like OS version, number of processors, RAM available, username in use, domain name, machine name and similar.

After that, the program will check if you have installed applications that are currently supported. Here is the list:




  1. Evernote


  2. Google Chrome


  3. Microsoft OneNote


  4. Mozilla Firefox


  5. Mozilla Thunderbird


  6. Pidgin


  7. Steam


  8. World of Tanks


The next stop: copying some data! Here's the list of applications and a current list of sensitive data it will copy:


  1. Evernote – file containing victim's current username, email associated with that username and a copy of victim's current database (implementing it right now).


  2. Google Chrome – files containing bookmarks, cookies, history, login data and web data.


  3. Microsoft OneNote – the copy of all of the victim's notebooks.


  4. Mozilla Firefox – files containing cookies, addons, form history and downloads history.


  5. Mozilla Thunderbird – files containing addons, address book and cookies (planning on supporting of copying all of the emails if a victim uses POP3 instead of IMAP).


  6. Pidgin – file containing all of the victim's usernames and passwords in clear text and a directory where victim's logs are saved.


  7. Steam – configuration file containing a list of all users ever connected on that PC and some decryption keys (not sure what those are for, but I will find it out).


  8. World of Tanks – file containing all of your preferences and a folder containing your latest battle results.


So, the program will automatically locate your removable drive and store all of those files in it.

The point of doing that program is to prove that a lot of pretty sensitive data is easily accessible to someone who has a physical access to your Windows machine. Combine those two and the victim gets pwned big time. The program is currently in pre-alpha stage and I don't recommend anyone using it for now, but if anyone wants to look at the code for now, you can do that [here](https://github.com/aleksandar-todorovic/SensitiveDataGrabber). Once it's finished, it will be open source (licensed under GPL) and everyone will be able to add programs to the compatibility list.
