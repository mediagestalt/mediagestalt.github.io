---
layout: post
author: Sandra Schwab
title: Handy Python Definitions
tags: 
- python
---

_updated on {{ site.time | date_to_long_string }}_

Lists all the files in a complex directory: 

{% highlight python %}

#this definition creates a recursive list of all files in the specified directory
def listFiles(dir):
    rootdir = dir
    for root, folders, files in os.walk(rootdir,topdown=False):
        for file in files:
            yield os.path.join(root,file)
    return
{% endhighlight %}

