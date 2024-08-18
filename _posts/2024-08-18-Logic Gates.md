---
layout: page
title: Digital Electronics No.1 - Logic Gates
description: Post No.1 from the Digital Electronics series
date: 2024-08-18
tags: Electronics
categories: Digital-Electronics-Course
---
<style>
th, td {
  border:1px solid black;
  text-allign: center;
  padding: 4px, 12px;
}
</style>

Digital electronics is a core aspect of modern technology, focusing on systems that use digital signals rather than continuous ones. In simpler terms, instead of working with smooth, varying signals like in analog electronics, digital electronics deals with distinct values—typically just 0s and 1s. This digital approach allows for the creation of reliable and flexible devices, from everyday gadgets like smartphones and computers to intricate communication systems. By using components like logic gates and microprocessors, digital electronics forms the backbone of the digital world, driving advancements and innovation in countless applications.

In this series I intend to teach you the basics of Digital Electronics

---

## Logic States
It is worth it to remind you that each input or output of a gate can have 3 states, "HIGH", "LOW" & "FLOATING".

- **HIGH** can mean **TRUE**, **1**, and in electronics **Positive Current**
- **LOW** can mean **FALSE**, **0**, and in electronics **Negative Current**
- **FLOATING** is a state which is unique only to actual electronics, it is used to denote that the pin is not connected and can have any value. It is essential for you to make connections in such a way that no pin is left empty as it may cause uncertain errors by randomly switching between **HIGH** and **LOW**

# Basic logic gates

All logic gates can be expressed in terms of 2 logic gates, **AND** and **NOT**. With the sole exception of a **BUFFER** gate which is used in to increase voltage and power.

### AND gate

The usual **AND** gate has 2 inputs and 1 output but there are others which can have more than 2 inputs. Those **AND** gates are simply a structure of the simpler 2-input **AND** gate similar to a binary tree. All **AND** gates have 1 output.

The Output of the **AND** gate is **HIGH** whenever all of the inputs of the gate are **HIGH**

#### Truth Table

| A | B | X |
|:-:|:-:|:-:|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 | 

### NOT gate

It is also commonly referred to as an **INVERTOR**. It has only 1 input and 1 output. The output is always the inverse of the input

#### Truth Table

| A | X |
|:-:|:-:|
| 0 | 1 |
| 1 | 0 |

### BUFFER gate

It is used in a way similar to a relay. Unlike relays instead of controlling Higher voltage circuits using a lower voltage circuit, it converts a low voltage signal into a high voltage signal.

#### Truth Table

| A | X |
|:-:|:-:|
| 0 | 0 |
| 1 | 1 |

### Tri-state BUFFER gate

A unique variation of a buffer with a second input, specifically referred to as the enable pin. This new pin essentially disables and enables the gate allowing control for when the buffer gives an output or not.

#### Truth Table

| EN | A | X |
|:--:|:-:|:-:|
| 0  | 0 | 0 |
| 0  | 1 | 0 |
| 1  | 0 | 0 |
| 1  | 1 | 1 |