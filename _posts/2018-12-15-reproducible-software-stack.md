---
title: "Reproducible Software Stack"
date: 2018-12-15
tags: [Reproducible, data science]
header:
  image: "/images/perceptron/percept.jpg"
excerpt: "Tools that faciliate and promote reproducibility "
---
You may have hear this echoing in those conferences that "Data Science is a
team sport". So how do you go about collborating when each members of the team
working on their PC? What ran on my machine might not run on yours

Replicating what someone else has done is his or her digital environment is the
starting point for collaboration.

### repo2docker

It takes URL to a Git repository (You already should have this as part of your
workflow) and creates a suitable Docker image.

It gives data scientists the benefits of containerization technology without
needing to learn Docker itself.

Thereby enable you to replicate data science environments and share it, allowing
your team to verify the results of analyses.

[Link](https://repo2docker.readthedocs.io)

### Checkpoint

This R package from Microsoft is designed to make it easy to write reproducible
R code by allowing you to go backward (or forward) in time to retrieve the exact
versions of the packages you need.

https://mran.microsoft.com/documents/rro/reproducibility

### MyBinder

MyBinder are JupterHub with repo2Docker. It lets you host interactive Jupyter
notebooks that you can share. It's a site that runs IPython/Jupyter Notebooks
from GitHub for free

[Resource](https://mybinder.readthedocs.io/en/latest/faq.html#user-memory)
limits maximum 2GB RAM, 10 minute inactivity timeout, 12 hour session.
