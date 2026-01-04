---
layout: post
title: UWB Positioning Board
description:  This is part of my Capstone project in my final year at Queen’s. The project is an indoor, gesture controlled drone swarm, and it is done in a group of four. My contribution is the indoor positioning, which uses Ultra-Wideband chips to allow each drone in the swarm to localize in a local coordinate system, defined by the placement of the “anchor” nodes. 
skills: 
  - PCB Design 
  - Impeadance Matching 
  - MCU Bring up 
  - Hardware Debugging 
  - Firmware/Software Debugging 
  - Integration 
  - Project Management 
main-image: /pcb.png
---

### The Problem

UWB positioning technology is needed in indoor environments due to the lack of GPS signals inside buildings. These systems are available off the shelf, however they are often very expensive, which was not suitable due to our limited budget. Therefore, there was a need for a low-cost UWB localization solution. These boards were designed using KiCAD, they are four layers (signal, ground, power, signal), and are flashed and debugged via a USB-C connection to the STM32F0 chip. Once the hardware design was complete and the boards came in, I assembled the boards and then began flashing them after hardware verification. The boards run open-source firmware that was modified to be tailored to our application. 

{% include image-gallery.html images="Image.jpg" height="400" %}
