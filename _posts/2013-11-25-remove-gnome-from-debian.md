---
layout: post
title: "Remove Gnome from Debian"
description: "how to remove Gnome package from Debian"
category: archive
tags: [Debian, apt-get]
image:
   feature: texture-feature-03.jpg
---

Today I requested a new Debain VM from our support team at the company; unfortunately the only available
template was Debian+Gnome, so the VM had gnome installed which is consuming lot of space without any actual
need for it, to clean up this mess I had to run this simple command 
{% highlight bash %}
apt-get autoremove --purge gnome* gdm* nautilus* libgnome* totem* gstreamer*; aptitude purge "~c"
{% endhighlight %}

That's all folks, gnome and all the desktop applications have been removed, along with all the config files
