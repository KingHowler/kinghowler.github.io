---
layout: page
title: Logical Line Follower
description: A line follower bot, made without any microcontrollers
img:
importance: 1
category: Coming Soon
tags: Electronics
related_publications: false
pretty_table: true
---

<style>
th, td {
  border:1px solid black;
}
.vector-gate {
  background-color: white;
}
</style>

# Why?
The project is being made as an educational project. I am building it to gain hands-on experience with **digital electronics** and **embedded systems**.

# What's new?
Almost all line follower projects use a microcontroller, namely the Arduino. I have already done that, now I am making a line follower bot that doesn't use an Arduino or any other microcontrollers, but instead it uses a custom logic circuit made using the 74XX IC Series

## The ICs being used

| IC no  | IC name             |
|--------|---------------------|
| 7404   | **HEX INVERTER**    |
| 7408   | **QUAD 2-INPUT AND**|
| 74279  | **QUAD SR LATCH**   |