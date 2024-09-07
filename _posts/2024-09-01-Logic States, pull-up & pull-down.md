---
layout: page
title: Logic States, pull-up & pull-down
description: Lecture 2 of Digital Electronics Course
date: 2024-09-01
tags: Electronics
categories: Digital-Electronics-Course
---

Before you know how to make actual digital electronics, there is one more thing that you need to know. What are the 3 possible logic states and how do I use them in my circuits?

---

# Logic States

There are 3 logic states:

1. **HIGH**
   - A **HIGH** logic state can sometimes also be referred as **ON**, **1**, **Positive Current**
   - It simply means that this pin is **Active**
2. **LOW**
   - A **LOW** logic state can sometimes also be referred as **OFF**, **0**, **Negative Current** or even **Grounded**
   - It simply means that this pin is **Inactive**
3. **FLOATING**
   - Floating may also be referred as **Not Connected** or **Undefined**
   - It is a state that occurs when the pin is not connected to a source or drain. It means that there is no precise logical state and that it can be either 1 or 0

---

## Floating State

Today the topic of our discussion will be the **Floating** State.

**What are the effects of floating state on the circuit?**

- The **FLOATING** state causes errors in the circuit's logic by randomly changing values and not triggering circuits as expected.

**What causes a floating state to occur?**

- The **FLOATING** state is caused by shoddy wiring and poor design.
- It can also occur due to hardware malfunction but it is best to look for faults in the wiring before deciding to change all of the hardware.

**How to ensure floating state doesn't occur in my circuit?**

- This brings us to our other topic of discussion for today, **Pull-up** and **Pull-down**.

---

### Pull-up

Pull-up refers to attaching the pin to a source or a positive current through a resistor. This means that the pin will always be in the **HIGH** state unless a negative current is passed. It is important to use resistor to avoid a short circuit between the pull-up and the input.

Below is an example where a pin has been pulled up. A pushbutton attached to GND is acting as the input.

{% include figure.liquid path="assets/img/dec/pull-up and pull-down/Pull-Up.png" title="PULL-UP" class="img-fluid rounded z-depth-1" %}

---

### Pull-down

Pull-down refers to attaching the pin to a drain or GND through a resistor. This means that the pin will always be in the **LOW** state unless a positive current is passed. It is important to use resistor to avoid a short circuit between the pull-down and the input.

Below is an example where a pin has been pulled down. A pushbutton attached to VCC is acting as the input.

{% include figure.liquid path="assets/img/dec/pull-up and pull-down/Pull-Down.png" title="PULL-DOWN" class="img-fluid rounded z-depth-1" %}

---

## When to use which?

Using **Pull-up** and **Pull-down** depends entirely upon your input. If you wish to send **LOW** as your input to the pin then you should use **Pull-up**, and if you wish to send **HIGH** as your input then you should use **Pull-down**.
