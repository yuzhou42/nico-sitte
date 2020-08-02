---
# Project title.
title: Unmanned Ground Systems Challenge

# Date this page was created.
date: "2016-03-01T00:00:00"
# Project summary to display on homepage.
summary: 

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags:
- UGV
- Robotics
- Autonomous Robot 
- Computer Vision
- Localization
- ROS

# Optional external URL for project (replaces project detail page).
external_link: 

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides: "`.
slides: 

# Links (optional).
url_pdf: 
url_slides: 
url_video: 
url_code: 

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack: fab", icon="twitter", name="Follow", url: https://twitter.com/georgecushen"}]

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
image:
  # Caption (optional)
  caption: 
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point: Smart
  preview_only: true
toc: true
---
Along with 3 other teammates from the [State Key Laboratory of Robotics](http://english.sia.cas.cn/rh/rp/201408/t20140814_125856.html), 
I participated in the Unmanned Ground Systems Challenge in October 2016 and worked specifically on the environment map 
building and localization under GPS signal lost situation.

This challenge was held in a real field environment, 
including wild battlefield task execution, 
city battlefield search and investigation, and highland transportation. 

![This is an image](ugv_1.png)
<center>Fig. 1. Our UGV platform</center>

### Environment Map


Built an environment map for non-structured fields with the following steps:

![This is an image](Slide6.png)
<center>Fig. 2. Environment Map BUilding Procedure</center>

The laser data was collected from different lasers: single-line, 32-line, and 64-line. 
The data was fused after calibration and having manually filled certain points.

![This is an image](Slide7.png)
<center>Fig. 3. Fuse Laser Data</center>

A road plane was fitted with a RANSAC method.
![This is an image](Slide8.png)
<center>Fig. 4. Point Clouds Segmentation</center>

The grid map was built with the help of the [grid_map](https://github.com/ANYbotics/grid_map) package. 
Finally, the road target was extracted through road skeleton extraction from the image generated from the environment map.

![This is an image](Slide9.png)
<center>Fig. 5. Road Target Extraction</center>

Thus, we obtained all the perception information needed to drive a car intelligently in a field environment.

{{< youtube id="AUbdU3WGoK8">}}
<center>**Obstacle Avoidance Demo**</center>

### Localization without GPS


Two methods were conducted to meet the requirements. 


#### 1. Visual Inertial Odometry


I did this by combining the orb slam with IMU.
![This is an image](Slide10.png)
<center>Fig. 6. Visual Inertial Odometry</center>

{{< youtube id="RRAzWU1_SSE">}}


#### 2. Laser Odometry   

{{< youtube id="c0VvjAZcUNo">}}


