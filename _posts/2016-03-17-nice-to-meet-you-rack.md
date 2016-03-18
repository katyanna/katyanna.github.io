---
layout: post
title: Nice to meet you, Rack
date: 2016-03-17 22:05:00
categories: learning programming challenge ruby rack TIL
---

Rails has always been around in my time with Ruby, to be honest I'm not really sure if I know how Ruby looks like out of Rails. Reason why I went looking for a way to use pure Ruby. After some research, I came to the conclusion that reeeeally pure Ruby would be too hardcore right now (due to having to deal with low-level HTTP/server stuff) and Rack is the answer I was looking for.


### What is Rack

[Rack](https://rack.github.io/) is a standard interface that defines the communication between web servers and the Ruby application. According to [RubyDoc](http://www.rubydoc.info/github/rack/rack/master/file/README.rdoc):

> Rack provides a minimal, modular, and adaptable interface for developing web applications in Ruby. By wrapping HTTP requests and responses in the simplest way possible, it unifies and distills the API for web servers, web frameworks, and software in between (the so-called middleware) into a single method call.


### Hello, Rack!

To use it you need an object that takes the env hash as a parameter and returns an array with the HTTP status, the HTTP header (it describes the response body) and the response body (the output of the application).

Install it by running `gem install rack` on your terminal. Create a `config.ru` file and insert the line above in it.

{% highlight ruby %}
run Proc.new { |env| ['200', {'Content-Type' => 'text/html'}, ['Hello, Rack \ (^. ^) /']] }
{% endhighlight %}


On command line, run `rackup config.ru` then go to [http://localhost:9292](http://localhost:9292/).

That's it! You have your first Rack app.