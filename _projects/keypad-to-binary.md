---
layout: page
title: Keypad to binary
description: Embedded system to convert input from keypad to binary number
img:
importance: 1
category: Coming Soon
tags: Electronics
related_publications: false
---

# In Progress

---

A completely raw electronics projects for converting a keypad button input from a 3x4 Membrane Keypad into a 4 digit Binary output.

---

# Module 1

## KeyPad Controller

#### Submodule 1: Clock Circuit

This module will generate a 20-30Hz square wave which will be used along with submodule 2 to help control the keyboards input and help differentiate between the buttons on the keypad.

> Items
>
> - 555 Timer IC chip
> - 120 nano Farads capacitor
> - 100 Ohms Resistor
> - 300k Ohms Resistor

#### Submodule 2: 3 bit Ring Counter

This module will ensure only 1 of the columns of the keypad will be used for taking an input at a certain time

> Items
>
> - 3 D Flip Flops

# Module 2

## KeyPad Decoder

This module will take inputs from the keypad to decode it into Binary. It will work using around 10 AND Gates and a lot of diodes

> Items
>
> - 10 AND Gates
> - Roughly 40 diodes

# Module 3

## Binary to 7 segment display

This module is used to produce a digit on a 7 Segment Display from 4 bit binary. This module will be used to display the output produced from the Keypad-to-Binary project

> Items
>
> - 7 segment display
> - BCD to 7 segment IC
