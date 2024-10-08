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

{% include figure.liquid path="assets/img/lfr/Side.jpg" class="img-fluid rounded z-depth-1" title="Side-View" %}

{% include figure.liquid path="assets/img/lfr/Front.jpg" class="img-fluid rounded z-depth-1" title="Side-View" %}

### Algorithm

{% include figure.liquid path="assets/img/lfr/Optimized Control Flow.png" class="img-fluid rounded z-depth-1" title="Optimized Control Flow" %}

**The code is designed on the basis of "correct and exit", It tries to correct any errors it finds and exit as soon as possible so that it can restart and get updated data swiftly and act accordingly**
**This will minimize the time spent with a certain reading and hence increasing the "Refresh Rate" of the program**
