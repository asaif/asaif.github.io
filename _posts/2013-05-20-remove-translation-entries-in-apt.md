---
layout: post
title: "remove translation entries in apt-get"
description: "Disable translations in apt-get"
category: archive
tags: [Debian, apt-get]
image:
 feature: texture-feature-05.jpg
---
One of the most great thing about Debian is it's package management system apt-get; one of it's powerful features comes for the ability
to customize it easily with small line of code, if you have a slow connection you will definitely need to prevent apt from checking for translations
every time you run apt-get update as it will take long time, plus you wouldn't really make use of them in most of the normal cases unless you are using
another language rather than English.
To disable apt-get translations do the following
{% highlight bash %}
echo -e "Acquire::Languages "none";" >> /etc/apt.conf
{% endhighlight %}
You can apply the above fix also on distro based upon Debian GNU/Linux as it will save you time and extra bandwidth you are losing during downloading unneeded translations.
