---
layout: post
title: "Use Nemo as default file manager"
description: "how to set Nemo as default file manager for Gnome"
tags: [Debain, Gnome]
categories: [archive]
image:
    feature: texture-feature-06.jpg
---

Two days ago I've upgraded my laptop from Debian Wheezy to Jessie, lot of new features are shipped with Jessie and I was very statisfied till I used Nautilus.
The new Nautilus is ugly and useless!! It doesn’t have status bar, no compact list view and more over the backspace key does not work any more and you’ll have to use arrow keys to navigateI used to love the old one, but the new version is compeleltly useless at least for me, after a few monoments searching for a good altrnative I found Nemo :), which is Linux Mint fork of Nautilus. which bring me back all the good features I used to love in Nautilus.

The follwoing steps descibe how to install Nemo and use it as the default file-manager for Gnome instead of Nautilus.

Install Nemo 

{% highlight bash %}
sudo apt-get install nemo
{% endhighlight %}

Set Nemo as the default file-manager

{% highlight bash %}
xdg-mime default nemo.desktop inode/directory application/x-gnome-saved-search
{% endhighlight %}

Set Nemo as the default handler for Desktop

{% highlight bash %}
gsettings set org.gnome.desktop.background show-desktop-icons false
{% endhighlight %}

{% highlight bash %}
gsettings set org.nemo.desktop show-desktop-icons true
{% endhighlight %}

Now your default file manager is Nemo, and your desktop is now handeld by Nemo isntead of Nautilus.
