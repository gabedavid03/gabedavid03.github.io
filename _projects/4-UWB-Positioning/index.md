---
layout: post
title: UWB Positioning Board
description:  This project is part of my Capstone project in my final year at Queen’s University. The project is an indoor, gesture-controlled drone swarm, and it is completed in a team of four. My contribution is the indoor positioning, which uses Ultra-Wideband chips to allow each drone in the swarm to localize in a local coordinate system, defined by the placement of the “anchor” nodes.

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

## The Problem

UWB positioning technology is needed in indoor environments due to the lack of GPS signals inside buildings. These systems are available off-the-shelf; however, they are often very expensive, which was not suitable for our team due to our limited budget. Therefore, there was a need for a low-cost UWB localization solution. The boards use the STM32F0 chip along with the DWM1000 UWB transceiver to send and receive RF signals. The board also features an EEPROM flash to store settings for each board and a barometer, and have multiple peripherals broken out to be expanded into a larger application. The board is powered, flashed and debugged over USB-C, allowing for an easy connection to any laptop. They were designed using KiCAD and are four layers (signal, ground, power, signal). Once the hardware design was complete and the boards came in, I assembled the boards and then began flashing them after hardware verification. The boards run open-source firmware that was modified to be tailored to our application.

{% include image-gallery.html images="Image.jpg" height="400" %}
