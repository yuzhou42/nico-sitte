---
# Project title.
title: Toward Autonomy of Micro Aerial Vehicles in Unknown Environments

# Date this page was created.
date: "2020-06-01T00:00:00"
# image_preview:featured.jpg
# Project summary to display on homepage.
summary: We present a comprehensive design and implementation for a micro aerial vehicle (MAV) that is able to perform 3D autonomous navigation and obstacle avoidance in cluttered and realistic unknown environments without the aid of GPS and other external sensors or markers.

# Tags: can be used for filtering projects.
# Example: `tags = [machine-learning, deep-learning]`
tags:
- UAV
- Robotics
- Autonomous Robot 
- Motion Planning
- Mapping
- GPU
- VIO
- ROS

# Optional external URL for project (replaces project detail page).
external_link:

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides:example-slides` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides:`.
slides:

# Links (optional).
url_pdf:
url_slides:
url_video: https://www.youtube.com/watch?v=KUKzsnORm-4&t=24s
url_code:

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack:fab, icon=twitter, name=Follow, url:https://twitter.com/georgecushen}]

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
image:
  # Caption (optional)
  caption:
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point: Smart


---
Since January 2019, I have been working on developing a  MAV system that can navigate autonomously in GPS-denied and obstacle-cluttered environments. Various advanced technologies have been designed, including a stereo visual-inertial state estimation that can handle scenarios without external localization resource, a GPU-based EDF mapping that significantly improves the real-time performance without sacrificing accuracy as well as a model predictive local motion planning with BSCPs solved by PSO, providing increased performance for tasks that require precise and timely maneuver. The results of simulation and real flight testing in both indoor and semi-open scenarios with various tasks have proved the effectiveness of the proposed system for challenging practical applications.

This work has resulted in the paper “Towards Autonomy of Micro Aerial Vehicles in Unknown and Global Positioning System Denied Environments” published in the IEEE Transactions on Industrial Electronics.



{{< youtube id="KUKzsnORm-4">}}
<center>Demo</center>






