---
layout: post
title: "I need a git cheatsheet"
date: 2015-11-15 10:00:00
categories: git cheatsheet
---

Frequently forget how to do certain things on git, so I'm just gonna keep putting them here for later consulting.

### Undo last commit

{% highlight shell %}
$ git commit -m "Something terribly misguided"
$ git reset --soft HEAD~
$ git add .
$ git commit -c ORIG_HEAD #uses last commit message
{% endhighlight %}

<br />


### Bring branch to master

#### On master

{% highlight shell %}
$ git fetch origin master
$ git rebase FETCH_HEAD
$ git checkout cool-feature-branch
$ git rebase master
#fix what may have broken
$ git checkout master
$ git merge cool-feature-branch
{% endhighlight %}
