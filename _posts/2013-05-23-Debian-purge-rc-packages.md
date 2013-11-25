---
layout: post
title: "Purge debian packages marked with rc status"
description: "how to purge rc status packages on debian"
category: archive
tags: [Debian, apt-get]
image:
   feature: texture-feature-03.jpg
---
On Debian packages marked with “rc” status, are packages not completely removed from the system, as it still have some configuration files.
To list the packages with “rc” status, use the following command:
{% highlight bash %}
 dpkg -l | grep '^rc'
{% endhighlight %}

To remove those packages, use the following command:
{% highlight bash %}
aptitude purge "~c"
{% endhighlight %}
Now all the configuration files for those packages have been removed, and there will be no referance any more for any of those packages.
