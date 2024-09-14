---
layout: page
title: Attendance System
description: An RFID based Attendance System using NodeMCU, integrated with an SQL server.
img:
importance: 1
category: Robotics
tags: Robotics
related_publications: false
repositories:
  - KingHowler/NodeMCU-Attendance-system
icons:
  - arduino/arduino-original.svg
  - php/php-original.svg
  - postgresql/postgresql-original.svg
  - mysql/mysql-original.svg
---

# Overview

An online attendance system made using the **NodeMCU**. The project uses **RFID** (Radio-Frequency Identification) with indicator lights, to record student attendances. A webpage handles the registration of new RFID tags under the name of the student. A second webpage is used to get the attendance records of the entire student body. The system is secure and has 3 custom "**Keys**" to ensure there is no access to any third party or false records made by someone with malicious intents.

## Summary of Features

1. **RFID**: modern, fast and accurate system
2. **LED Indicators**
3. **Registered students only**
4. **Security Keys** : Ensure a controlled access
   - Key #1 : For marking attendance of students, possessed by "**School Certified**" attendance recorders
   - Key #2 : For viewing the attendance record of the entire school body, possessed by school administration
     - For a "key-less" viewing of the attendance record, the student must state it's registration ID (Personal RFID assigned by administration). This will allow the student to see his own attendance records only
   - Key #3 : For registering new tags, possessed by school administration
5. **SQL Server** : All records are stored on an SQL server and can hence be modified as the administration wills to

# Code Overview

<div style="background-color : #000000">
  {% include figure.liquid path="assets/img/attendance-sys/Arduino-main.svg" title="Arduino Main Code" width="900px"%}
</div>
