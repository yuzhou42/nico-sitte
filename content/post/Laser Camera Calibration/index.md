---
title: Laser Camera Fusion
date: "2017-01-01T00:00:00"
summary: This project was to calibrate the translation and rotation matrices between camera and laser coordinate systems to provide laser points with color information from the image for further applications such as segmentation.
tags:
- Laser 
- Sensor Fusion 
- Computer Vision
- ROS
  
url_code: https://github.com/NicoChou/camera-laser-calibration
image:
  focal_point: Smart
---

This project was to calibrate the translation and rotation matrices between camera and laser coordinate systems 
to provide laser points with color information from the image for further applications such as segmentation. 

The QR code board was used as a marker, which could be detected in both point clouds and image. 
I matched the center point pair of the QR code from the 2D points in the image and that of the 3D points in laser coordinates, 
and used the PnP method to get the relation between the two coordinates. 
The calibration procedure and fusion results are shown on Figure 1.

![This is an image](featured1.png)
<center>Fig. 1. Calibration Procedure<center>


{{< youtube id="9jwvK2DOzgU">}}
<center>Video 1. Fusion results<center>


{{< youtube id="ihkgXOpipxY">}}
<center>Video 2. Fusion results<center>