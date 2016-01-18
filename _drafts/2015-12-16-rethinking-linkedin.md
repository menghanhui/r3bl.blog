# Rethinking LinkedIn for (for software developers)

Today, I've got yet another spam from LinkedIn telling me:

> You are among a special group of members selected to receive a free 30-day trial to lynda.​com.

Everyone who ever used LinkedIn knows that this email is just plain bullshit. Everyone gets 30 day trial to Lynda. To get access to this trial, you have to give LinkedIn your credit card info and they'll charge you after 30 days if you don't cancel your service, which, even though it became a standard, is not a proper way to run the trial (basically, you're relying on people giving you their credit card info and later on forgetting about that).

So, after I tweeted a small rant...

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">I cannot wait to see LinkedIn dying. There&#39;s not a thing about them that I don&#39;t despise.</p>&mdash; Aleksandar Todorović (@r3bl_) <a href="https://twitter.com/r3bl_/status/677147527699898369">December 16, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

...I have decided to give myself a little thought about what I like about LinkedIn and what I don't like (or absolutely despise) with the goal of re-imagining LinkedIn for software developers. Here's what I came up with.

## Things I like about LinkedIn

* You get the same design for every profile you decide to visit (you don't have to search through the website to find what you want).
* You're mostly going to see the same categories in all of the profiles.
* You can apply for jobs using your LinkedIn profile.
* You can search for a job nearby.

## Things I don't like about LinkedIn

(This list is way longer)

* It constantly asks you to enter your email password (which is just bullshit, you absolutely do not need access to my email account what so ever)
* You're constantly going to be "among a special group of members" that's going to receive some spam.
* You're constantly annoyed to enter some section that you have no interest in adding to your LinkedIn profile. Even though I did not have any formal work experience, I had to make something up just to stop LinkedIn from annoying me. Now that I actually got my first job, I haven't posted it on LinkedIn because I see no value in doing so (at least for now).
* You're constantly being added as a colleague by random people you have never met and you're never going to meet.
* Lots of endorsements =/= being actually skilled in that area. I'm being endorsed in some areas I have no real experience in just because I have listed them. As a software developer, you're not going to amaze a recruiter by having a bunch of endorsements. That's just not how software development field works.
* No actual way to showcase your code.
* Messaging options are a gigantic mess.
* Even though my "Profile Strength" is currently at the "All-Star" level, LinkedIn just keeps pushing me towards entering even more junk section and therefore making it harder for anyone to search for actually relevant content (no LinkedIn, no recruiter gives a fuck about which courses did I take in my college).
* It's centralized.
* Profile customization ability is very limited (yes, I know that this directly interferes with one of the LinkedIn pros I have listed above).
* ...

Now, let's look at the current LinkedIn alternatives and see their flaws.

## Personal website / Portfolio

* You have to make an effort to design your own website even if your HTML5/CSS3/JavaScript/Bootstrap/AngularJS/Responsive design/WordPress/server management/AddWhateverWebTechnologyIsMainstreamAtTheMoment skills are not that great.
* Things are not uniquely designed, so you're going to find same sections in different places.
* Sometimes you won't find the info you actually need.
* You can write anything you want. Recruiters are going to have a tough job verifying things you've posted.

## GitHub profile (and generators that generate your resume through GitHub)

* Even though I have >750 contributions in the last year, the reality is that probably 500 of them are actually updates to my site (since [I'm hosting it on GitHub](https://github.com/aleksandar-todorovic/aleksandar-todorovic.github.io)) and to [my notes](https://github.com/aleksandar-todorovic/notes/).
* I have about 750 pushes more organized in private repositories that I have no actual way of showing.
* The tech team I'm a part of uses [GitLab](https://about.gitlab.com/) to develop most of the things we're developing. Our GitLab is not publically exposed because it's full of tools that are not open source at the moment. We usually decide to open source them and release them [on our GitHub's organization profile](https://github.com/occrp/) later on, but then, all of our commits are gone and you cannot actually see who of us made what.
* There's absolutely no way to showcase proprietary software in your GitHub profile.
* I can put on my resume that I was the very first person in the world whose pull request got accepted to the NSA's GitHub profile, even though [I literally capitalized a single letter](https://github.com/NationalSecurityAgency/SIMP/commit/d67b8ce12970b1be536fbb2358774243a43abe5f) in my pull request.
* There's no way of showing your job history or... well, pretty much anything else except your code.

## Re-imagining LinkedIn

So, let's see. What do actually job recruiters seek when they're looking for a software developer? I could be wrong, but I think that the answer is the following:

* Actual code
* Work experience
* Technologies a person is familiar with
* Involvement in other people's projects
* A couple of recommendations from former colleagues
* A couple of highlighted blog posts / scientific papers / other types of writing
* Contact details

I think that every other type of information is just redundant and has absolutely no value to the recruiters.

So, what does a software developer usually have where he can showcase this?

* Website / blog / portfolio
* GitHub account
* LinkedIn account
* StackOverflow account (or some other StackExchange account)

Of course, I'm not saying that every developer has these resources, but I think that most of the developers rely on these specific web services while they're developing something.

Out of these four sources, I think that GitHub has the potential of satisfying most of the requirements I have listed. I'll explain the details in a minute.

## Potential challenges

* In one of the requirements (recommendations from other people) there should be a way to verify that the person who wrote the recommendation is indeed a person who the potential job recruiter said he is.
* The whole thing should be easy to set up.
* It should be reasonably well designed (mobile first), and yet, it should be fast to load.
* It should be decentralized as much as possible.

## What I have tried before

To make some sense out of my GitHub profile, Dal Jaenis [proposed](https://wiselike.com/dal-jeanis/questions/should-i-clean-my-github-profile-to-make-my-code-more-approachable-to-the-recruiters?focus=561b4c9da788d12a4d5fff02) that I should create a GitHub project called [recruitMe](https://github.com/aleksandar-todorovic/recruitMe) that will guide potential recruiters through my GitHub contributions in an easy way. Unfortunately, that turned out not to be that easy to sum up.

## What I think we should try
