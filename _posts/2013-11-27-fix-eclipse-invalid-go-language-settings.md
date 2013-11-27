---
layout: post
title: "Fix eclipse invalid go language settings"
description: "Fix eclipse go language settings"
tags: [Golang, Eclipse, Debian]
category: Archive
image:
    feature: texture-feature-06.jpg
---

One of the great things about eclipse, is that it have multiple plugins for different lanaguges which make it my favorite IDE. 

During the last few days I was exploring Go language, and have installed eclipse plugin for it, unfortuantly it pop up an pleasent meassage
saying "eclipse invalid go language settings", here are the steps I've done to fix this issue:

* Open Eclipse
* Go to Window-> Preferences
* Select Go, and set the valuse as following:
    * GOROOT: /usr/lib/go
    * GOPATH: /usr/share/go
    * Go-tool path: /usr/bin/go
    * Go formatter: /usr/bin/gofmt
    * Go documentor: /usr/bin/godoc


Create a new Go project, and enjoy coding Go in eclipse.

**Note:** The go pathes may differ if you compiled and installed go manually, those are the pathes for golang installed from Debian repos.
