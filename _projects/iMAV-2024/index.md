---
layout: post
title: iMAV 2024 Competition
description:  This was a team project for the iMAV 2024 Micro Air Vehicle Competition that took place in Bristol, UK in September 2024. Myself and my teammates represented the Queen’s University Aerospace Design Team, placing 2nd out of the fully undergraduate teams in the competition. This project was mainly worked on during the summer leading up to the competition, mainly during the evenings after we were all done at our respective co-ops. 
skills: 
  - Gazebo Simulation
  - Simulated Sensors (Camera, LIDAR) 
  - Simulated Actuators (Motors)
  - PX4 Autopilot 
  - CMAKE Tools 
  - SDF 
  - Blender 
  - Simulation to Real Transistion 
  - System Integration and Debugging 

main-image: /IMG_5202.JPEG
---

## Creating the Simulation
One of the big problems we faced was the need for a  a high-fidelity simulation to mirror our drone’s hardware and competition settings as closely as possible. This required forking PX4 Autopilot firmware to create a digital twin of our drone with the needed sensors and motor constants. The camera and 1D LIDAR integrated well in Gazebo, however there were serious troubles integrating an optical flow sensor and making it work with the flight controller’s simulated algorithm. Later, during integration, we figured out it was due to the fact that the optical flow sensor has to be manually enabled in the terminal on the flight controller.

## The Final Product 
Aside from the simulation, we develloped a state machine and line following control logic for the drone to complete the competition tasks. The competition was a drone "obstacle course” where the drone had to follow a line until it read an AruCo marker, which signified a different task. Our logic first found the lines laid out on the ground, projected a virtual circle down on the line, and then found the intersection point of the line and circle. This gave us both the direction of the line and whether it was ahead or behind of the drone. After integrating all of these elements in the simulation for testing and refining, the group unfortunately had to split up for co-op. We continued working virtually, and then met at the competition for integration and real life testing where we ran into many issues with our line following control before our flight window. We managed to iron these issues out, performing well in competition. 