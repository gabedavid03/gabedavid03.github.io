---
layout: post
title: iMAV 2024 Competition
description:  This was a team project for the iMAV 2024 Micro Air Vehicle Competition that took place in Bristol, UK in September 2024. My teammates and I represented Queen’s University Aerospace Design Team, placing second out of all the undergraduate teams in the competition. My team did the majority of the work on this project during the summer leading up to the competition, mainly throughout the evenings after we were all done at our respective co-ops.
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

{% include image-gallery.html images="full_sim.png, test_sim.png" height="350" %}

## Creating the Simulation
One of the big problems my team faced was the need for a high-fidelity simulation to mirror our drone’s hardware and competition settings as closely as possible. This required forking PX4 Autopilot firmware to create a digital twin of our drone with the necessary sensors and motors. The camera and 1D LIDAR integrated well in Gazebo, however there were serious troubles integrating an optical flow sensor and making it work with the flight controller’s simulated algorithm. Later, during integration, we figured out it was because the optical flow sensor must be manually enabled in the terminal on the flight controller. The next part of the simulation entailed recreating the whole competition course in simulation. The competition was laid out as an obstacle course, with the drone being required to follow a line and then complete different tasks based on the AruCo Marker on the line. The whole competition was simulated to validate our line following, state machine, and task execution.

<video
  autoplay
  muted
  loop
  playsinline
  style="
    width:50%;
    height:400px;
    object-fit:cover;
    border-radius:8px;
  ">
  <source src="/_projects/3-iMAV-2024/line_follow.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Our Approach 
Our approach to line following used the intersection of the line with a virtual circle projected from the drone onto the floor. Using this intersection point, we could determine both the direction of the line and whether it was in front of or behind the drone. This allowed for consistent heading reference as well as easy heading correction during navigation on the line. From there, when the drone detected an AruCo Marker, the state machine would then transition into the state for the task that the AruCo Marker identified. This included flying through gates, landing in precise positions, taking photos of specific locations and sending them back to ground control. Initially this was all done in simulation. We then transitioned to the hardware at competition to validate our algorithms on the real course during our test flights.

{% include image-gallery.html images="air-bnb-test.jpeg, comp1.JPG, comp2.JPG" height="350" %}

## The Final Product 
Due to resource constraints, it was difficult to completely reproduce the competition course in the real world before going to the UK. As a result, we had limited time to test and tune our algorithms to the real world. During our test flight windows, we noticed discrepancies in our simulation and how the drone behaved in real life. This turned out to be a coordinate system mismatch, which mainly affected the line following logic and the PID controls of the drone. As such, we set up a makeshift “competition course” in our AirBNB at the competition site to finalize our algorithm before competition. This allowed the team to iron out the major issues before competition and left us placing second among all undergraduate teams on competition day. Overall, this was a great learning experience, and we were quite proud of our results.

## The Team 
Myself, Grant Keefe, Ian Keefe, Conor Spalvieri, Ryan Berry. 
