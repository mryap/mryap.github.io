---
title: "Formatting options for Docker commands"
date: 2018-12-23
tags: [Dockers]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "set a default format so you don't have to type the same thing in every time,
nor constantly resize your terminal"
---

###

Docker looks for a config file in `~/.docker/config.json`.

It stores settings here, like

* auth credentials (which in Docker 1.11 you will be able to move auth creds
  elsewhere...)
* custom format for `docker ps`

![image](https://user-images.githubusercontent.com/15719191/50384937-50c5ae80-06c4-11e9-947b-535da36aab53.png)

The configuration that I use for the above `docker ps` format

    # Configuration that I use:
    {
    "psFormat": "table {{.Names}}\\t{{.Image}}\\t{{.RunningFor}} ago\\t{{.Status}}\\t{{.Command}}"
    }
