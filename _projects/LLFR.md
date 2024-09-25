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

| IC no. | IC name              |
| ------ | -------------------- |
| 7404   | **HEX INVERTER**     |
| 7408   | **QUAD 2-INPUT AND** |
| 555    | **555 Timer IC**     |

## 555-bistable 5-bit memory for storing the current state of the bot

{% include figure.liquid path="assets/img/llfr/Memory-unit.jpeg" title="Memory Unit" class="img-fluid rounded z-depth-1" %}

Next I will make a Control Unit using Inverters and diodes.

## The 5 states

| State | Full Name                |
| ----- | ------------------------ |
| LF    | **Left - Full speed**    |
| LH    | **Left - Half speed**    |
| FF    | **Forward - Full speed** |
| RH    | **Right - Half speed**   |
| RF    | **Right - Full speed**   |

## The Control system

**NOTE : "ANOS" means "AND NO OTHER STATES"**

### I/O

| Inputs | Purpose                   |
| ------ | ------------------------- |
| A      | **Very Left sensor**      |
| B      | **Slightly Left sensor**  |
| C      | **Middle sensor**         |
| D      | **Slightly Right sensor** |
| E      | **Very Right sensor**     |

### State Saver

| State | Entry      | Exit          |
| ----- | ---------- | ------------- |
| LF    | A **ANOS** | C             |
| LH    | B **ANOS** | A + C         |
| FF    | C **ANOS** | A + B + D + E |
| RH    | D **ANOS** | C + E         |
| RF    | E **ANOS** | C             |
