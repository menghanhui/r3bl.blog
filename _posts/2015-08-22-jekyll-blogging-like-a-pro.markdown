---
author: Aleksandar Todorović
comments: false
date: 2015-08-22 15:17:00+01:00
layout: post
slug: jekyll-blogging-like-a-pro
title: "How to create a website/blog using Jekyll and GitHub pages (tutorial)"
categories: en
tags:
- tutorial
- GitHub
- Jekyll
image:
  feature: abstract-1-3
---

I've been hosting my blog using GitHub Pages + Jekyll combination for about eight months now. I learned some advantages and disadvantages of using these tools, so I thought I should create a guide on how to become Jekyll poweruser (and use GitHub for hosting your websites).

## What is Jekyll?

Jekyll is a static site generator that allows you to create a blog or a website without having to worry about complicated administrative tools, databases etc. Jekyll stores everything inside of text files. It allows you to publish your posts using Markdown markup language (we'll talk about that later). It's completely free and open source. If you have a GitHub account, you can host your site completely free and have full control. Unlike Wordpress.com, pretty much every theme is free and there are no restrictions on which theme you can use with it. Your blog won't be serving ads unless you want it to and you can change everything you want to on your site just by having a basic HTML knowledge.

## What you'll need to have/know follow this tutorial

* A GitHub account (obviously)
* A local machine running Linux with Git installed (`sudo apt-get install git` is all you need). You'll also need to [set up your Jekyll environment](http://jekyllrb.com/docs/quickstart/). I should point out that Jekyll doesn't officially support Windows, but if you have a Mac, that's fine too.
* Some basic `bash` knowledge (you'll need to know how to navigate between directories using `cd` command)
* A custom domain (optional)

## Things GitHub allows you to do

GitHub allows you to create one custom domain that has to be named `USER.github.io` where `USER` is obviously your GitHub username. You can think of it as a central place for your website. If you have a GitHub organization, you can create another URL which will be titled `ORG.github.io`. You can also create websites for your specific open source projects which will be hosted at `USER.github.io/PROJECT`.

**Note:** Everything I say further about user's website can be applied to organization's websites as well.

## Creating a website for you or your organization

To create your main website (`USER.github.io`) you will need to create a repository specifically titled `USER.github.io` (note: your username doesn't have to be capitalized). Then, from the terminal on your local machine, execute this command:

`git clone https://github.com/USER/USER.github.io`

This command will create a subfolder titled `USER.github.io`. Navigate inside of it and create a new file called `index.html` (you can create a file using the following command `touch index.html`). Now, lets actually write some HTML code. Open up the file in your favorite text editor and type this:

`<h1>Testing</h1>`

Save the file, open up your terminal one more time, navigate to the `USER.github.io` directory and execute the following commands:

```
git add index.html
git commit -m 'Initial commit'
git push
```

These commands will sync your local folder with your website. The first command will add the `index.html` file to your project, the second command will commit your changes and set `Initial commit` as a message for the commit, and the third line will push those changes back to GitHub.

After this is done, just wait for a couple of minutes and open `http://USER.github.io` in your browser.

## Setting up a custom domain

Feel free to skip this section if you don't want to use a custom domain.

Now, if you have your own domain that you want to use, create a new file called `CNAME`. In it, just type in your domain. I own a [r3bl.me](http://r3bl.me) domain, so the content of my CNAME file contains `r3bl.me` and nothing else. Note that the `http://` and `https://` should not go here. After this is done, before you publish your changes, you'll need to edit the CNAME records on your hosting provider. I'm personally using [Namecheap](https://www.namecheap.com/) so my CNAME records look like this:

![picture1]()

The full content of the `IP ADDRESS/URL` field is actually `aleksandar-todorovic.github.io.` (pay close attention to the dot at the end which is necessary) since aleksandar-todorovic is my GitHub username.

After this is done, after a couple of minutes, your domain should successfully load the content of the `index.html` file we created earlier.

## Setting up Jekyll

Now we have the domain set up, it's time to actually build a Jekyll site. Before doing so, delete the `index.html` file you created earlier. We don't need it anymore.

Now, you have two options: you can create a default Jekyll site by typing `jekyll new .` in your terminal after navigating inside of your `USER.github.io` directory, or you can just copy the content of one of the Jekyll themes. Two of the best resources for custom Jekyll themes I found are [jekyllthemes.org](http://jekyllthemes.org/) and [jekyllthemes.net](http://www.jekyllthemes.net/) (note: these are two different sites even though they are using a similar domain).

Now, you need to push your changes back to GitHub:

```
git add .
git commit -m 'Initial Jekyll setup'
git push
```

You'll notice that the first command is a bit different. This time, we're not only adding one file, but we're adding the entire content of that directory.

After you've done so, in a couple of seconds you'll have a Jekyll site up and running on your `USER.github.io` or your custom domain and now you can start to customize your Jekyll site.

## Customizing your Jekyll site

This part of a tutorial is a bit tricky because the customization is different depending on a Jekyll theme you chose. Usually, it starts by editing the file called `_config.yml` which is the most important file in your Jekyll repository. In most of the cases, that's the place where you should set up things like the name of your site, your site's description, your social links and a list custom Jekyll plugins.

Before you publish the changes back to GitHub, you can preview the changes on your local machine by executing `jekyll serve` and then navigating to `127.0.0.1:4000` in your browser. To terminate the command, just press `Ctrl+C`.

## Publishing blog posts

To manage your blog posts, you'll need to know a simple markup language called Markdown. If you've ever used sites like reddit or StackOverflow, you already know it! Markdown is pretty easy to learn. It won't take you more than 20 minutes to learn it. Here are some basics:

* To add a title, just type `# Title of the post` on the top of your file.
* To add a subtitle, just type `## Subtitle`. To add a smaller subtitle, just add another `#`. You can have up to 6 `#` signs. The more you have, the subtitle will be smaller.
* Adding a link to the text: `[name of the link](http://pathtothelink)`
* Bold: `**this text will be bolded**`
* Italic: `*this text will be italicized*` (you can also use `_this text will be italicized_`).
* Adding an image: `![name of the image](http//pathtotheimage)`

Now that we got that covered, your posts should be stored in the `_posts` subdirectory. To create a new blog post, you'll need to follow this example: `2015-08-22-new-post.markdown`. So, the pattern you should follow while creating a new file should be: `year-month-day-name-of-the-post.markdown`. Sometimes, you'll need to add certain meta tags at the top of your file. Those tags should go right at the top of your file like this:

```
---
author: Aleksandar Todorović
layout: post
categories: en
tags:
- tag 1
- tag 2
- tag 3
---

# Markdown code goes here
```

The most usual meta tag is `layout: post` which tells Jekyll that it's rendering a blog post. Probably every Jekyll theme comes with a couple of default posts, so refer to their file and figure out which tags you should include.

## Publishing a page

It's a bit different to publish a page than it is to publish a blog post. Lets say that you want to create a page titled `about` which will be accessed through `USER.github.io/about`. You have two options: you can create a file in the directory of your project called `about.md` where you'll write some Markdown text, you can create a file called `about.html` where you'll write some HTML code, or you can create a new subirectory called `about` and create a new file called `index.html` or `index.md`. The result is the same: your page will be accessible by opening `USER.github.io/about` in your browser.

## Creating repository websites

The process for creating a website for your other repositories is pretty much the same with some minor differences.

Lets say that you have some sort of an open source project that became popular enough to need its own website. We'll call it `awesome`, because, well, your project is awesome. The difference this time is that you can't put your files in the `master` branch. You're going to have to create a new branch called `gh-pages`. This time, `git clone https://github.com/USER/awesome` will not get the job done. This time, you'll have to execute the following command to clone your website to your local machine:

`git clone https://github.com/USER/awesome -b gh-pages --single-branch`

This command will copy the specific branch called `gh-pages` and that's where the content of your website will be stored. After you've successfully set up your code, just repeat the commands we already talked about to sync your content with GitHub. After that, your website will be visible at `https://USER.github.io/awesome`.

Now if you have a custom domain and you want to use a subdomain for that website, you'll need to edit the CNAME records on your domain. Create a new subdomain (lets say `http://awesome.r3bl.me`) and point it to the same `USER.github.io.` URL. Now, in your `CNAME` file, add your subdomain (`awesome.r3bl.me`) and that's it. After a couple of minutes, your website will be available at `http://awesome.r3bl.me`.

## Some obstacles you're going to encounter with

* By hosting your website on GitHub pages, you can't create any databases. All you can use is HTML, CSS, JavaScript and a static site generator (like Jekyll).
* The code behind your website will be publicly accessible, so make sure not to store any valuable data in your repository. If you need to store some valuable data inside of your repository, you'll need to upgrade your GitHub account from free to paid and make your repository private so nobody else can access it. Your website will still be accessible, but your repository won't be.
* HTTPS support is... kind of complicated:
  * If you're using a `USER.github.io` domain, your website _is_ accessible by typing `https://USER.github.io`, but you can't enforce your visitors to use HTTPS exclusively, so you'll have to rely on them to use the HTTPS version. Maintaining both of HTTP _and_ HTTPS versions of your website was too complicated for me, so I gave up on that.
  * If you're using a custom domain, you can't buy and use an SSL certificate because it will be issued to your domain, not to your GitHub repository, so your certificate will appear as invalid while accessing your site from any major browser. This _can_ be kind of hacked by using [CloudFlare](https://www.cloudflare.com/). By signing up for a CloudFlare account (don't worry, it's free), you can change the nameservers on your hosting to their nameservers. Then, the traffic between the users and CloudFlare will be SSL encrypted, but the traffic between GitHub and CloudFlare will still not be encrypted. That's the best thing you can do.

## [Advanced] Some tips and tricks (in no particular order)

* If you have some string that you want to use regularly, put it in your `_config.yml` file. As an example, my Twitter account is [@r3bl_](https://twitter.com/{{ site.twitter }}) and I want to link to it often. I will just add a new `twitter: r3bl_` line to my `_config.yml` file and then put a link to it by typing `[@r3bl_](https://twitter.com/{{ site.twitter }})`. I could also put the entire link (`twitter: https://twitter.com/r3bl_`) to my config file and then use `[@r3bl_]({{ site.twitter }})` if I want to.
* If you're working on an article, but it's still not finished, you can create a new subdirectory called `_drafts` and put those articles there. After that, just move them to your `_posts` subdirectory to publish them.
* If you want to ping search engines every time you put some new content to your site, create a `gems: jekyll-sitemap` line to your `_config.yml`. This will create a sitemap on your site available on `USER.github.io/sitemap.xml` (or `blog.r3bl.me/sitemap.xml` in my case). This is a third party Jekyll plugin that GitHub supports.
* Create a file called `robots.txt` and put every page that you don't want to be indexed by search engines there. Take a look at the `robots.txt` [of my blog](http://blog.r3bl.me/robots.txt) as an example. To make sure search engines index only things that matter, search for `site:r3bl.me` and make sure to use their webmaster tools (I'm personally using only [Google's webmaster tools](https://www.google.com/webmasters/) and [Bing's webmaster tools](www.bing.com/webmaster/)).
* If you made some big changes to your site, you can ping Google manually by visiting `http://www.google.com/webmasters/sitemaps/ping?sitemap=http://example.com/sitemap.xml` (obviously, you'll need to replace `http://example.com` with your URL). You can do the same with Bing by using `http://www.bing.com/webmaster/ping.aspx?siteMap=http://example.com/sitemap.xml`.
* You can hack your way into supporting HTTPS by adding `{{ site.url | replace:'http://','https://' }}/SOMETHING">` to every link that points to another place on your website. Your site will still be accessible over HTTP, but every time somebody clicks some new URL, it will take him to the HTTPS version of the page.
* You can mess around with the look of your posts or pages by editing `_layouts/post.html` or `_layouts/page.html`.
* You can customize pretty much everything by editing the files in `_includes` and `_layouts` subdirectories. You don't have to pay attention to other directories. Here's the link to an original Jekyll theme called [HPSTR](https://mmistakes.github.io/hpstr-jekyll-theme/) that I used while I was creating my blog. Obviously, I made quite a number of changes.
