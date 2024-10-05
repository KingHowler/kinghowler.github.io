---
layout: github-project
title: Line Follower
description: A Line Follower bot using an Arduino.
img: assets/img/lfr/Icon.webp
importance: 4
category: Robotics
tags: Robotics
related_publications: false
repositories:
  - KingHowler/Line-Follower
github: https://github.com/KingHowler/Line-Follower
icons:
  - file: arduino/arduino-original.svg
    site: devicons
---

{% include video.liquid path="assets/videos/lfr/Demo.mp4" class="img-fluid rounded z-depth-1" title="Line Follower (No PID) Demo" autoplay=true loop = true %}

### Algorithm

{% include figure.liquid path="assets/img/lfr/Optimized Control Flow.png" class="img-fluid rounded z-depth-1" title="Optimized Control Flow" %}

**The code is designed on the basis of "correct and exit", It tries to correct any errors it finds and exit as soon as possible so that it can restart and get updated data swiftly and act accordingly**
