---
title: "Online Jupyter Notebook"
date: 2018-12-29
tags: [Jupyter]
excerpt: "Jupyter Notebooks as a Service- A free Data Science environment in the cloud."
---
RMOTR Notebooks bills itself as a Jupyter Notebooks as a Service. It allows you
to have a data science environment in the cloud. No need to spin up you own
virtual server on a cloud platform like AWS, GCP or Azure.

![image](https://user-images.githubusercontent.com/15719191/50531263-fa5ed280-0afe-11e9-81a2-bf05c02ea633.png)

My impression of  RMOTR Notebooks is the whole process is fast. The response is
instantaneous the moment you execute a cell of code or markdown in the browser.
It offers a generous 512MB RAM - 60 times more than the RAM on my laptop!

In the terminal, I export the packages that are available on RMOTR
Notebooks by using `pip freeze`

```Python
pip freeze > requirements.txt
```

<script src="https://gist.github.com/mryap/cdb190c307bfb564ef87da8ff78d502d.js"></script>
