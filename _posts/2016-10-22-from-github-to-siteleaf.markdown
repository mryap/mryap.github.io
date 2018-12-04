---
title: From GitHub to Siteleaf
date: 2016-10-22 00:00:00 Z
layout: post
---

Since 11th October, I have being using Barry Clark's Jekyll-Now to generate my site that hosted on GitHub. For the past weeks, http://mryap.github.io is being served from GitHub.

This early morning, I reconnect the GitHub repo via siteleaf.com just to see what the outcome. I like Siteleaf as it provides a web-based interface for managing content on GitHub. You can use it to create, edit, and delete files, and save your changes directly to GitHub via a web browser. 

This arrangement is useful if I need to bring in a collaborator who might not be well-versed editing markdown content on GitHub environment.  The files on this site is still residing on GitHub. 

This post is to test whether anything breaks as a result of my little experiments. 

### Addendum
To my dismal, when I use siteleaf.com, it mess up the so-called YAML front matter -  a snippets of code that looks like this

```
---
title: From GitHub to Siteleaf
date: 2016-10-22 00:00:00 Z
layout: post
---
```
The outcome is that while your new content (i.e. a Post or a page) being created on GitHub, it will not appear on your website. 
