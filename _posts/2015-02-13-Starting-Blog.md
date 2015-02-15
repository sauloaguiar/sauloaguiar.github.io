---
layout: post
title:  "Starting on Jekyll and Koding"
tags: Jekyll, blogging, web, Koding
comments: true
---

In this first blog post I'm going to describe how to you setup Jekyll in a Koding.com account.<!--more-->

To start this, make sure you already have your koding.com access. If you have some familiarity within linux terminal usage, it will be helpful too.

## Installing

### Prerequisites

Install ruby, ruby development libraries and the make helper.

{% highlight ruby %}
sudo apt-get install ruby ruby-dev make gcc node-js
{% endhighlight %}

We are also installing nodejs that is required by Jekyll. (See [issue](https://github.com/jekyll/jekyll/issues/2327))

### Jekyll

Now we can install the jekyll itself using

{% highlight ruby %}
sudo gem install jekyll
{% endhighlight %}

After having success, you can see the version running just typing

{% highlight ruby %}
jekyll -v
{% endhighlight %}

The output for me is jekyll 2.5.3

For more information about Jekyll, visit the project docs [1].

## Running

To start a new website from scratch you can type

{% highlight ruby %}
jekyll new mysite
{% endhighlight %}

whereas mysite will be the folder's name that will contain all site information. Now you can head into the folder and start the jekyll serve using

{% highlight ruby %}
jekyll serve -d /home/koding_username/Web
{% endhighlight %}

Here, we are using the -d option to inform Jekyll that we want our website to be generate at the specified directory. We are point to /home/koding.username/Web because [Koding provides web access](http://learn.koding.com/guides/where-is-my-webserver-root/) to this directory.

Now, look at your [koding.com assigned URL](http://learn.koding.com/faq/vm-hostname/) to access your new site. For instance, mine is http://uskk308e3f07.sauloaguiar.koding.io/. 


## Preparing for GitHub

On GitHub Pages documentation[2] there is a suggested way to run Jekyll in order to have a similar environment. To achieve this, we need to install two more things: Bundler and GitHub-pages gem.

{% highlight ruby %}
gem install bundler github-pages
{% endhighlight %}

Now, head into your site folder, and type

{% highlight ruby %}
bundler init
{% endhighlight %}

this will generate a Gemfile that you will need to update with

{% highlight ruby %}
source 'https://rubygems.org'
gem 'github-pages'
{% endhighlight %}

this will enforce jekyll to use github gem. Now, to run Jekyll in a way that matches the GitHub Pages, let's use Bundler.

{% highlight ruby %}
bundler exec jekyll serve -d /home/koding.username/Web
{% endhighlight %}

Good Job! Now, you have a fully functional and free way to edit your website.

## References

[1] [Jekyll Docs](http://jekyllrb.com/docs/home/)

[2] [Using Jekyll within GitHub Pages](https://help.github.com/articles/using-jekyll-with-pages/)

[3] [Nokogiri Troubleshooting](http://www.nokogiri.org/tutorials/installing_nokogiri.html)

[4] [Koding VM Hostname](http://learn.koding.com/faq/vm-hostname/)

[5] [Michael Chelen Blog](http://michaelchelen.net/81fa/install-jekyll-2-ubuntu-14-04/)
