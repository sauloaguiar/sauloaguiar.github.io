---
layout: post
title:  "Catching up on Android"
tags: Android, development, cats
comments: true
---

It's has been a while since I took some time to write/share about my learning experiences.<!--more-->

The idea stay the same. The commitment is a new one.
As I just made my way back to Brazil and I'm unemployed (yay!), I decided to enjoy the break and catch up
on my Android development skills.
My goal is to create an application that has a timeline of cute cats. What would be more enjoyable to do, right?
Hopefully, I will also help people to enjoy them whenever they have a break.

In order to create the application, I decided to use some tools/libraries that I guess are trending in the Android
community right now. Where did I grab them from? Well, I have the habit to check these four different sources:

* [Android weekly](http://androidweekly.net) - a weekly newsletter with - guess what - awesome android tips!
* [Caster](https://caster.io) - a very nice website with short and straight to the point tutorials.
* [Android Dialogs](https://www.youtube.com/channel/UCMEmNnHT69aZuaOrE-dF6ug) - cool youtube channel with interviews and fireside chats with android superstars and GDE's.
* [Fragmented Cast](http://fragmentedpodcast.com) - my preferred android podcast with awesome interviews/development tips.

So, to create the application I decided that I will have a [continuous integration](https://en.wikipedia.org/wiki/Continuous_integration) environment, a test suite - with [unit](https://en.wikipedia.org/wiki/Unit_testing) and ui tests, good code structure - I'm very biased to use [MVP](http://antonioleiva.com/mvp-android/) as the architecture pattern, and also some libraries to help the development: [picasso](http://square.github.io/picasso/) and [retrofit](http://square.github.io/retrofit/), for example.

I decided to create a very simple - and ugly - mockup to have an overall idea of how the application should look like.

![cute-cat-feed-screenshot]({{ site.url }}/assets/images/cute-cat-feed.png)


Within this said, next time I come back here, I will share how I did my continuous integration setup.
