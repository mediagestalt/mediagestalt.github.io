---
layout: post
author: Sandra Schwab
title: Renaming Thousands of Files with Terminal
category: tutorials
tags: 
- terminal
- bash 
- python
---

The problem: how to rename tens of thousands of image files (with varying file formats in a complex directory structure) from one specific name to another specific name while simultaneously copying all the files to a new folder, preserving the structure of the old directories.

{% highlight bash %}

cp # terminal
copy # command prompt

{% endhighlight %}

Sure you can just use this command to copy files from one place to another, but it also RENAMES the files too!


windows: need to create destination file first, otherwise there will be an error. Not so on Mac
output to file:

{% highlight bash %}

whatever.bat >logfile.txt 2>&1 # command prompt

bash whatever.sh >logfile.txt 2>&1 # terminal

{% endhighlight %}