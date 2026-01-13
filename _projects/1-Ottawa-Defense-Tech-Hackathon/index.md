---
layout: post
title: Ottawa Defense Tech Hackathon 2025
description:  "This was a team project for the Ottawa Defense Tech Hackathon that took place in November 2025. The goal of the Hackathon was to create a system to detect and classify UAVs based on their acoustic signature. By the end of the day, my team had a fully working prototype of our product, <i>Cerberus</i>, which was able to make detections in real time and publish to a GUI in order to easily view the detections each node made. My team won First Place in the competition, taking home the prize of $10,000."
skills:   
  - YAMNet
  - ML Classifiers (MLP, SVC, Random Forest, KNN)
  - Audio Processing 
  - Data Augmentation 
  - Log-mel Spectograms 
  - Technical Communication (Written and Oral)
main-image: /IMG_4428.JPEG
---

## Our Approach 
Based on the problem statement given out at the Hackathon, the team knew that our system had to run on the edge in a power- and resource-constrained environment. From there, we began to divide and conquer, with half of us working on our GUI and the other half doing research and development on different ML pipelines to classify the UAVs. My initial R&D was developing a pipeline using YAMNet-derived embeddings paired with trained downstream classifiers. This pipeline performed well; however, a pipeline developed in parallel by a teammate outperformed my pipeline in evaluation. This approach used YOLO on the log-mel spectrogram of the audio clips and was ultimately the method used in our system due to its performance and scalability. Once we made this pivot, I shifted my focus to our pitch presentation, working on communicating the team’s idea for the product through our slide deck and the presentation. The Team (left to right): Ian Keefe, Grant Keefe, Myself, Conor Spalvieri, Ryan Berry.

<iframe
  src="/assets/pdfs/Cerberus.pdf"
  width="100%"
  height="650px"
  style="border: none;">
</iframe>
