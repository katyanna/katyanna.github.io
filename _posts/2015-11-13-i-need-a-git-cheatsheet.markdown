---
layout: post
title: "I need a git cheatsheet"
date: 2015-11-15 10:00:00
categories: git cheatsheet
---

### Undo last commit
{% highlight shell-session %}
$ git commit -m "Something terribly misguided"
$ git reset --soft HEAD~
$ git add .
$ git commit -c ORIG_HEAD #uses last commit message
{% endhighlight %}

<br />

### Bring branch to master

####On master
{% highlight shell-session %}
$ git fetch origin master
$ git rebase FETCH_HEAD
$ git checkout branch
$ git rebase master
$ git checkout master
$ git merge branch
{% endhighlight %}
