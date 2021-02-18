---
layout: post
title: Deploying a Flask app to Google App Engine
date: 2017-05-22 15:05:00
categories: learning deploy gcloud flask python google appengine
---

This is the base file tree I use:
{% highlight shell %}
_ lib/
_ static/
\_ style.css
_ templates/
\_ index.html
_ main.py
_ appengine_config.py
_ app.yaml
_ requirements.txt
{% endhighlight %}

Ex: [GitHub - katyanna/kblog](https://github.com/katyanna/kblog)

`lib/`, `app.yaml` and `appengine_config.py` are needed for the App Engine. The rest is basic Flask.

* #### lib/
You will need to have the libraries files in this paste for the deploy to work nicely.
To install the required libs inside `lib/`, run:
{% highlight shell %}
$ pip install -t lib/ -r requirements.txt
{% endhighlight %}

* #### appengine_config.py
Where you can customize Python modules. You should define only the constants or hook functions you wish to override.

* #### app.yaml
It contains information about the application code.  You can also put the url handlers in this file.

* #### static / templates
Where Flask will look for your `.css` and `.html` files respectively.

* #### main.py
Your python code.

* #### requirements.py
The list of libraries you’ll use.

## Environment set up
**1.** Make sure you have Python 2.7.9 or later:
{% highlight shell %}
$ python -V
{% endhighlight %}

**2.** Download and install the Google App Engine SDK accordingly to this: [Google Cloud SDK](https://cloud.google.com/sdk/docs/)

**3.** Install the gcloud component that includes the extension for Python:
{% highlight shell %}
$ gcloud components install app-engine-python
{% endhighlight %}

**4.** Create a project:
{% highlight shell %}
$ gcloud create
{% endhighlight %}

## Deploying the app
**1.** Test your application
{% highlight shell %}
$ dev_appserver.py $PWD
{% endhighlight %}

**2.** Deploy it
{% highlight shell %}
gcloud app deploy app.yaml --project projetct-id
{% endhighlight %}

## My thoughts on App Engine
I didn’t enjoy it very much. Considering I’ve only worked with Heroku so far, I found App Engine to be much more complex than needed and inflexible. That’s my inexperienced opinion, if you have a thing or two to say in favor of App Engine, please comment so I can learn a little bit more.
