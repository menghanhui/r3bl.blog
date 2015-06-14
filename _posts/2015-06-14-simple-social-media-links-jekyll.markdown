---
author: Aleksandar Todorović
comments: true
date: 2015-06-11 20:10:00+01:00
layout: post
slug: simple-social-media-links-jekyll
title: "Simple way to integrate social media links into Jekyll website"
categories: en
tags:
- Jekyll
- blogging
- tutorials
image:
  feature: abstract-1-3
description:
---

I saw this error happening over and over in a lot of places. People do not integrate their social links using Jekyll. Instead, they hard code them into HTML code. Well, there's a better way and it's pretty simple.

## Prerequisites

Of course, the first prerequisite is to [install Jekyll](http://jekyllrb.com/docs/installation/). For those of you who don't know, Jekyll is as simple static site generator as it can get. It allows you to create a website without worrying about the things such as databases.

The second prerequsite is to install [Font Awesome](http://fontawesome.io/). Font Awesome is the most popular icon font out there and it contains hundreds of icons. The icon pack is fully open source, so you can use it in any project you want (for further information about the licenses used, [click here](http://fontawesome.io/license/)).

To include them in your project, open the `_includes` directory in the root folder of your project. Then, using your favorite text editor, edit the file `head.html`.

Include this line at the bottom of the file:

{% highlight html %}
{% raw %}
<link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">
{% endraw %}
{% endhighlight %}

That's it, you're done with setting things up.

## Creating variables for the icons

Edit your `_config.yml` file in the root directory of your file. There, you'll already see two variables, called `twitter_username` and `github_username`. Now, add more variables:

{% highlight html %}
{% raw %}
twitter_username:     r3bl_
github_username:      aleksandar-todorovic
linkedin_username:    aleksandartodorovic
google_plus_username: AleksandarTodorovićr3bl
facebook_username:    aleksandar.todorovic.r3bl
dribbble_username:
{% endraw %}
{% endhighlight %}

Of course, you'll need to replace my usernames with your usernames. If you don't use some social medias I listed, just leave the username blank and don't worry about it.

## Adding icons

Find an appropriate place where you want to show your icons. If you want to show them in your footer, edit the `footer.html` file from your `_includes` directory. If you want to add them somewhere in the main body of your website, edit `index.html` file from the root directory.

After you found the place, you're ready for your next step.

Create an unordered list using the `<ul></ul>` tag. Then, copy the codes below.

Now what these codes will do is they're going to check your `_config.yml` file you edited earlier. If they find an appropriate username, they will show the icon of that social network linking to your profile.

### Twitter code

{% highlight html %}
{% raw %}
{% if site.twitter_username %}
  <li>
    <a href="https://twitter.com/{{ site.twitter_username }}">
      <i class="fa fa-twitter"></i> Twitter
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

### GitHub code

{% highlight html %}
{% raw %}
{% if site.github_username %}
  <li>
    <a href="https://github.com/{{ site.github_username }}">
      <i class="fa fa-github"></i> GitHub
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

### LinkedIn code

{% highlight html %}
{% raw %}
{% if site.linkedin_username %}
  <li>
    <a href="https://linkedin.com/in/{{ site.linkedin_username }}"
      <i class="fa fa-linkedin"></i> LinkedIn
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

### Google+ code

{% highlight html %}
{% raw %}
{% if site.google_plus_username %}
  <li>
    <a href="https://plus.google.com/{{ site.google_plus_username }}">
      <i class="fa fa-google-plus"></i> Google+
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

### Facebook code

{% highlight html %}
{% raw %}
{% if site.facebook_username %}
  <li>
    <a href="https://www.facebook.com/{{ site.facebook_username }}">
      <i class="fa fa-facebook"></i> Facebook
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

### Dribbble code

{% highlight html %}
{% raw %}
{% if site.dribbble_username %}
  <li>
  <a href="https://dribbble.com/{{ site.dribbble_username }}" class="icon">
      <i class="fa fa-dribbble"></i> Dribbble
    </a>
  </li>
{% endif %}
{% endraw %}
{% endhighlight %}

## Final result

![screenshot](http://i.imgur.com/2yVPGnq.png)

Of course, this is the screenshot on the default Jekyll installation. If you're using a Jekyll theme, your result will look differently.

Note that I'm not using Dribbble. I left the variable `dribbble_username` blank in the `_config.yml` file, so the icon is not shown.

## What if you're not using some social media listed here?

You have two options. One is to not copy the code and the second one is to leave the variable in your `_config.yml` file blank. The result is the same: the icon will not be shown, as seen in the Dribbble example above.

## What if you're using some social media not listed here?

[Click here](http://fontawesome.io/icons/) to see all of the icons available in the Font Awesome pack. If your icon is not there, the best thing you can do is to search for the issue [in the repository](https://github.com/FortAwesome/Font-Awesome/issues). If you find it, add a comment supporting the idea. If you don't find it, create a new issue.

## Further customization of the icons

Refer to the [examples](http://fontawesome.io/examples/) of using Font Awesome pack. You can make them bigger, animate them, rotate them and a whole lot more.

## Need help?

Just leave the comment below. I'll be more than happy to help you out.
