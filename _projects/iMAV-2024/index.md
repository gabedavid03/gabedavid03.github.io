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

{% include image-gallery.html images="full_sim.png, test_sim.png" height="250" %}

## Creating the Simulation
One of the big problems we faced was the need for a high-fidelity simulation to mirror our drone’s hardware and competition settings as closely as possible. This required forking PX4 Autopilot firmware to create a digital twin of our drone with the needed sensors and motors. The camera and 1D LIDAR integrated well in Gazebo, however there were serious troubles integrating an optical flow sensor and making it work with the flight controller’s simulated algorithm. Later, during integration, we figured out it was due to the fact that the optical flow sensor has to be manually enabled in the terminal on the flight controller. The next part of the simulation entailed recreating the whole competition course in simulation. The competition was layed out as an obstacale course, with the drone needing to follow a line and then complete different tasks based on the AruCo Marker on the line. The whole compeition was simulated to validate our line following, state machine, and task execution. 

<video
  controls
  autoplay
  muted
  loop
  playsinline
  style="width:50%; max-width:50%; border-radius:8px;">
  <source src="/_projects/iMAV-2024/line_follow.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

{% include image-gallery.html images="air-bnb-test.jpeg" height="250" %}

## Our Approach 
Our approach to line following used the intersection of the line with a vritual circle projected from the drone onto the floor. Using this intersection point, we could determine both the direction of the line and whether it was it was in front or behind the drone. This allowed for consistent heading reference as well as easy heading coreection duing navigation on the line. From there, when the drone detected an AruCo Marker, the state machine would then transition into the state for the task that the AruCo Marker identified. This included flying through gates, landing in presice positions and taking photos of specific locations and sending them back to ground control. Initially this was all done in simulation, transistioning to the hardware at competition to validate our algorithms on the real course during our test flights. 

{% include image-gallery.html images="comp1.JPG, comp2.JPG" height="250" %}

## The Final Product 
Due to resource contraints, it was difficult to completely reproduce the competition course in the real world before going to the UK, thus we had limited time to test and tune our alorithms to the real world. During our test flight windows, we noticed discrepencies in our simulation and how the drone behaved in real life, this turned out to be a coordinate system mismatch which mainly affected the line following logic, as well as the PID controls of the drone. As such, we set up a makeshift "compeition course" in our AirBNB at the compeition site to finalize our algorithm before comeptition. This let us iron out the major issues before compeition, and left us placing 2nd among undergraduate teams on compeition day. Overall, this was a great learning expiernce and we were quite proud of our results. 

## The Team 
Myself, Grant Keefe, Ian Keefe, Conor Spalvieri, Ryan Berry. 
