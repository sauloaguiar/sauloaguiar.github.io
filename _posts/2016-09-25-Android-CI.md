---
layout: post
title:  "Setting the project environment"
tags: Android, development, circleci, Continuous-integration
comments: true
---
Alright, next step onto making the project happen! Setting up the continuous integration environment.<!--more-->

As I mentioned in the last post, my goal with this application is to learn more about the whole development process and improve my skill set.
The first step that I decided to take was to create the new Android project - following the Android Studio wizard - and add it right away to a continuous integration service.
This time, I'm experimenting with [circle ci](https://circleci.com). They have a free tier for single users - with some limitations of course - but it will be enough for my needs.

I decided to watch this short introductory video from [caster.io](https://caster.io/episodes/episode-2-android-continuous-integration-with-circleci/) so I could have an overall idea of how the setting up would work and it has helped a lot.

Basically, you have three steps to follow:
1. Create and share your android project in github repo
2. Create an account on circle ci using and granting access to your github account
3. Import the android project in the circle ci panel.

After you do the third step, circleci will immediately start a build using your repo. Now it's time to create a circle.yml file for our project. Depending on the project, circleci maybe smart enough to get your configurations, but in my recent experiences with android projects, it wasn't able to do.

So let's start with this [sample file](https://gist.github.com/donnfelker/7189cad9c6654f918e7e) provided by [donnfelker](http://www.donnfelker.com). Make sure you add the file to the root level of your project, otherwise circleci won't be able to load the information stored on it.
You can read more info about the structure and contents of the file in [circleci configuration page](https://circleci.com/docs/configuration/).

Also, if you want to fire testing after you build is correctly done, you will need to customize the steps that circleci takes. Refer to the [circleci android page](https://circleci.com/docs/android/) for more details on it. I will try to write about this after I add tests to my project.
