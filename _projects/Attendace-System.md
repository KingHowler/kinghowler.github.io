---
layout: github-project
title: Attendance System
description: An RFID based Attendance System using NodeMCU, integrated with an SQL server.
img: assets/img/attendance-sys/Top-view.jpeg
importance: 1
category: Robotics
tags: Robotics
related_publications: false
repositories:
  - KingHowler/NodeMCU-Attendance-system
github: https://github.com/KingHowler/NodeMCU-Attendance-system
icons:
  - file: arduino/arduino-original.svg
    site: devicons
  - file: php/php-original.svg
    site: devicons
  - file: mysql/mysql-original.svg
    site: devicons
---

# General Overview

An online attendance system made using the **NodeMCU**. The project uses **RFID** (Radio-Frequency Identification) with indicator lights, to record student attendances. A webpage handles the registration of new RFID tags under the name of the student. A second webpage is used to get the attendance records of the entire student body. The system is secure and has 3 custom "**Keys**" to ensure there is no access to any third party or false records made by someone with malicious intents.

---

## Summary of Features

1. **RFID**: modern, fast and accurate system
2. **LED Indicators**
   - Green LED : Student marked as present successfully
   - Yellow LED : Student already marked as present
   - Red LED : Student not recognized
3. **Registered students only**
4. **Security Keys** : Ensure a controlled access
   - Key #1 : For marking attendance of students, possessed by "**School Certified**" attendance recorders
   - Key #2 : For viewing the attendance record of the entire school body, possessed by school administration
     - For a "key-less" viewing of the attendance record, the student must state it's registration ID (Personal RFID assigned by administration). This will allow the student to see his own attendance records only
   - Key #3 : For registering new tags, possessed by school administration
5. **SQL Server** : All records are stored on an SQL server and can hence be modified as the administration wills to

---

# Code Overview

## NodeMCU-Code

<div align="center" style="background-color : #FFFFFF" class="img-fluid rounded z-depth-1">
  {% include figure.liquid path="assets/img/attendance-sys/NodeMCU-main.svg" title="NodeMCU Main Code" max-width="500px" %}
</div>
<div align="center" style="background-color : #FFFFFF" class="img-fluid rounded z-depth-1">
  {% include figure.liquid path="assets/img/attendance-sys/NodeMCU-sub.svg" title="NodeMCU Sub Code" max-width="500px" %}
</div>

---

## Server-Code

<div align="center" style="background-color : #FFFFFF" class="img-fluid rounded z-depth-1">
  {% include figure.liquid path="assets/img/attendance-sys/PHP.svg" title="Server-side PHP Code" %}
</div>

---

# Circuit Overview

## This is the circuit for an Attendance Recorder

{% include figure.liquid path="assets/img/attendance-sys/Circuit.png" title="Circuit Diagram" class="img-fluid rounded z-depth-1" %}

---

## The Attendance Recorder

{% include figure.liquid path="assets/img/attendance-sys/Top-view.jpeg" title="Top view" class="img-fluid rounded z-depth-1" %}
{% include figure.liquid path="assets/img/attendance-sys/Side-view.jpeg" title="Side view" class="img-fluid rounded z-depth-1" %}

---

## The RFID Tags

{% include figure.liquid path="assets/img/attendance-sys/Tags.jpeg" title="Tags" class="img-fluid rounded z-depth-1" %}
