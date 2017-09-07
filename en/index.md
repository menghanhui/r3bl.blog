---
layout: page
title: "Content I wrote in English"
comments: true
share: false
image:
  feature: abstract-1-3
---

## On other websites

<ul>
    <li><a href="https://opensource.com/life/15/9/ato-interview-garth-braithwaite">Open source is ugly: Improving UI and UX</a> (Interview with Garth Braithwaite from Adobe), published on <a href="http://opensource.com">Opensource.com</a> (September 22, 2015)</li>
    <li><a href="http://opensource.com/education/15/9/what-attracts-students-to-your-project">9 ways to attract students to your open source project</a>, published on <a href="http://opensource.com">Opensource.com</a> (September 11, 2015)</li>
    <li><a href="http://opensource.com/life/15/9/interview-don-schenck-rackspace">Rackspace developer advocate on getting started with open source</a> (Interview with Don Schenck), published on <a href="http://opensource.com">Opensource.com</a> (September 2, 2015)</li>
    <li><a href="https://opensource.com/business/15/8/interview-daniel-roesler-utilityapi">Why every website should switch to HTTPS</a> (Interview with Daniel Roesler), published on <a href="http://opensource.com">Opensource.com</a> (August 21, 2015)</li>
    <li><a href="https://opensource.com/life/15/8/interview-ken-starks-texas-linux-fest">The problem with Linux text-to-speech (TTS)</a> (Interview with Ken Starks), published on <a href="http://opensource.com">Opensource.com</a> (August 19, 2015)</li>
    <li><a href="http://opensource.com/life/15/8/gnome-turns-18">18 reasons to use Gnome on its 18th birthday</a>, published on <a href="http://opensource.com">Opensource.com</a> (August 15, 2015)</li>
    <li><a href="http://opensource.com/life/15/7/interview-ben-balter-github">Open source licensing at GitHub</a> (Interview with Ben Balter from GitHub), published on <a href="http://opensource.com">Opensource.com</a> (July 10, 2015)</li>
    <li><a href="http://opensource.com/life/15/6/my-linux-story-Aleksandar-Todorovic">Linux as a lifestyle</a>, published on <a href="http://opensource.com">Opensource.com</a> (June 30, 2015)</li>
    <li><a href="http://opensource.com/business/15/6/interview-cat-robson-red-hat">Open source licensing important for future of Internet of Things</a> (Interview with Cat Robson from Red Hat), published on <a href="http://opensource.com">Opensource.com</a> (June 17, 2015)</li>
    <li><a href="http://opensource.com/life/15/2/beginners-guide-github">A beginner's guide to GitHub</a>, published on <a href="http://opensource.com">Opensource.com</a> (February 16, 2015)</li>
</ul>

## On my own blog

<ul>
    {% for post in site.categories.en %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})</li>
    {% endfor %}
</ul>
