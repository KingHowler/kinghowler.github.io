---
layout: page
title: Basic Logic Gates and Truth Tables
description: Lecture 1 of Digital Electronics Course
date: 2024-08-25
tags: Electronics
categories: Digital-Electronics-Course
featured: false
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

For this lecture let's start with the very basics.

#### What is Digital Electronics?

It is the branch of physics which deals with logic signals and the electronic components that produce them. It includes usage of boolean algebra, logic circuits and ICs which have complex transistor logic implemented inside them. It is somewhat similar to Computer Engineering.

---

## Truth Tables

A truth table shows every single possible input combination and the respective outputs for each. For example, an AND Gate has the following Truth Table:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 0        |
| 0       | 1       | 0        |
| 1       | 0       | 0        |
| 1       | 1       | 1        |

> Don't worry I will be explaining what an AND gate is as well

In digital electronics, 1 denotes "ON" while 0 denotes "OFF"

> The meaning of 1 and 0 will be described in more detail in `Lecture #2: Logic States, pull-up & pull-down`

---

# The 6 Basic Logic gates

## AND gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/AND.svg" title="AND" class="img-fluid rounded z-depth-1" %}</div>

The **AND** gate has 2 inputs. When both of the inputs are set to 1, only then will the output also result in 1.

The Truth Table for an **AND** gate is as follows:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 0        |
| 0       | 1       | 0        |
| 1       | 0       | 0        |
| 1       | 1       | 1        |

<br><br>

## NOT gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/NOT.svg" title="NOT" class="img-fluid rounded z-depth-1" %}</div>

The **NOT** gate has 1 input. In it the output is always the exact opposite of the input

The Truth Table for a **NOT** gate is as follows:

| Input A | Output Q |
| ------- | -------- |
| 0       | 1        |
| 1       | 0        |

<br><br>

## OR gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/OR.svg" title="OR" class="img-fluid rounded z-depth-1" %}</div>

The **OR** gate has 2 inputs. If any of the inputs is 1, then the output also result in 1.

The Truth Table for an **OR** gate is as follows:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 0        |
| 0       | 1       | 1        |
| 1       | 0       | 1        |
| 1       | 1       | 1        |

<br><br>

## NAND gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/NAND.svg" title="NAND" class="img-fluid rounded z-depth-1" %}</div>

The **NAND** gate has 2-inputs. It is basically a **NOT** gate connected to the output of an **AND** gate. When both of the inputs are set to 1 only then will the output result in 0.

The Truth Table for a **NAND** gate is as follows:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 1        |
| 0       | 1       | 1        |
| 1       | 0       | 1        |
| 1       | 1       | 0        |

<br><br>

## NOR gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/NOR.svg" title="NOR" class="img-fluid rounded z-depth-1" %}</div>

The **NOR** gate has 2-inputs. It is basically a **NOT** gate connected to the output of an **OR** gate. When both of the inputs are set to 0 only then will the output result in 1.

The Truth Table for a **NOR** gate is as follows:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 1        |
| 0       | 1       | 0        |
| 1       | 0       | 0        |
| 1       | 1       | 0        |

<br><br>

## XOR gate

<div class="vector-gate">{% include figure.liquid path="assets/img/dec/logic-gates/XOR.svg" title="XOR" class="img-fluid rounded z-depth-1" %}</div>

The **XOR** gate is sometimes also referred to as the "Exclusive OR gate". It has 2-inputs and when both of the inputs have different values. only then will the output also result in 1.

The Truth Table for an **XOR** gate is as follows:

| Input A | Input B | Output Q |
| ------- | ------- | -------- |
| 0       | 0       | 0        |
| 0       | 1       | 1        |
| 1       | 0       | 1        |
| 1       | 1       | 0        |

---

### Multi-Input Logic Gates

The Logic Gates **AND, OR, NAND, NOR, XOR** all have 2 inputs, but it is not uncommon to see these same logic gates with a different number of Inputs. This is because the circuit is arranged in a certain way that the form a "Tree-like" structure.

For example, a 4-input **AND** gate is basically an **AND** which has each of it's 2 inputs connected to the outputs of two other **AND** gates, effectively emulating as a single 4-input **AND** gate instead of a 4-input Logic Circuit.

The Truth Table for such a circuit would be as follows:

| Input A | Input B | Input C | Input D | (A **AND** B) E | (C **AND** D) F | Output Q (E **AND** F) |
| ------- | ------- | ------- | ------- | --------------- | --------------- | ---------------------- |
| 0       | 0       | 0       | 0       | 0               | 0               | 0                      |
| 0       | 0       | 0       | 1       | 0               | 0               | 0                      |
| 0       | 0       | 1       | 0       | 0               | 0               | 0                      |
| 0       | 0       | 1       | 1       | 0               | 1               | 0                      |
| 0       | 1       | 0       | 0       | 0               | 0               | 0                      |
| 0       | 1       | 0       | 1       | 0               | 0               | 0                      |
| 0       | 1       | 1       | 0       | 0               | 0               | 0                      |
| 0       | 1       | 1       | 1       | 0               | 1               | 0                      |
| 1       | 0       | 0       | 0       | 0               | 0               | 0                      |
| 1       | 0       | 0       | 1       | 0               | 0               | 0                      |
| 1       | 0       | 1       | 0       | 0               | 0               | 0                      |
| 1       | 0       | 1       | 1       | 0               | 1               | 0                      |
| 1       | 1       | 0       | 0       | 1               | 0               | 0                      |
| 1       | 1       | 0       | 1       | 1               | 0               | 0                      |
| 1       | 1       | 1       | 0       | 1               | 0               | 0                      |
| 1       | 1       | 1       | 1       | 1               | 1               | 1                      |
