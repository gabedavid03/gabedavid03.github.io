---
layout: post
title: School Robotics Projects
description:  This page includes projects that I have worked on for classes as a part of my BASc in Mechatronics and Robotics Engineering at Queens's University, or competitions I’ve taken part in at Queen’s.  

skills:   
  - Technical Communication (Written and Oral)
main-image: /IMG_3512.JPEG
---

## Final Year Capstone Project
For my final year capstone project, my group and I are building a gesture-controlled autonomous indoor drone swarm. Over the course of this project, there is a mix of both technical and non-technical work. At the beginning of the project, my team broke it down into four subsystems: ground UWB modules, drone UWB modules, path-planning, and machine learning and human machine interface. I am working on the ground UWB subsystem and system integration. This includes hardware design, MCU bring up and firmware development, as well as integration with the drones UWB modules and ensuring accurate positioning. 

## Queen's Engineering Competition
In second year and third year, three friends and I participated in the Queen's Engineering Competition. It is a one-day competition where teams are given a problem and set materials in the morning, and then by the end of the day the team must present their prototype to a panel of judges for grading. While in our second year we sadly we did not make the podium, in our third year we came in third place. 

## Mechatronics and Robotics Design
This is a semester-long class that occurs every year for Mechatronics and Robotics students. Each year, the professor comes up with a different robotics-based problem involving hardware and software designs that students need to solve in groups of 2-4. These problems are always open-ended, and it is exciting to see how my classmates have approached the same problem each year. 

### Mechatronics Design III 
This class’s design challenge was more mechanically focused than in previous years. We were given basic components and sensors for a small autonomous robot and told to design a robot that uses these electrical components to line follow until a certain checkpoint and then be controlled by a game controller to pick up small dolls and deliver them safely to a checkpoint. This was supposed to simulate a “Jurassic Park”-style rescue mission.  My groupmate and I designed the robot in OnShape and combined both 3D printed parts with laser cut MDF board to manufacture the robot. All the code was written in C++, and the electrical system was built using breadboard components and jumper wires.  

### Mechatronics Design II 
This year’s design challenge was much more software-oriented and was my first introduction to ROS. At the start of the term, we were given a robot chassis along with a base electrical system including a battery, Arduino, raspberry pi, LiDAR, motors, and environmental sensors. On top of these components, we could add whatever we wanted to the project. The goal of this project was to create a small mobile robot that autonomously navigates a room and maps the CO<sup>2<sup> concentrations of the room in different places. In this project, I worked on the autonomy stack using SLAM with the LIDAR to map and navigate the room, integrating the CO<sup>2<sup> sensor readings to create a live updating heatmap. I faced some issues with the autonomous navigation during the project, and by the end of the project the robot sadly could not operate fully autonomously. The robot was, however, able to update the live heatmap via its reading while controlled with a game controller. This project was a very fun one to work on, and I learned a lot about robotics and integration throughout the process. 

### Mechatronics Design I 
This project was an introduction to autonomous mobile robots. It was a diff-drive robot made of Lego with motors controlled by an Arduino to follow a line, pick objects up, drive around the board and then deliver them to the other side. Looking back, this project taught me the basics of sensor integration and embedded programming, using the line following sensor readings to create control loops to stay on the line, and build turn subroutines. On top of this, I learned how to control motors, and combine these into a functioning system. 

## Other 
Simulated PLL (LTSpice), Autonomous Dog Feeder (Python, C++, Hardware Prototyping), Minesweeper (C), Knights Traversal (C).  
