---
title: "Visual Target Detection and Tracking Framework Using Deep Convolutional Neural Networks for Micro Aerial Vehicles"
authors:
- Mingjie Lao
- Xudong Chen
- Feng Lin
- Geng Qin
- Wenqi Liu
- nico # put this author name instead of your name directly will enable the function of showing your Info at the end of the publication page

date: "2018-06-22T21:44:14+08:00"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2018-06-22T21:44:14+08:00"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In * International Conference on Control and Automation (ICCA)*, IEEE.
publication_short: In *ICCA*
abstract: This paper presents a visual detection and tracking framework which estimates a smooth target position for various applications on micro aerial vehicles (MAVs). The proposed framework consists of two major components, a deep learning-based detector and a correlation ﬁlter-based tracker.The detector running at a low frequency ﬁrst detects a targetand initializes the tracker. The estimated target position from the tracker will be updated by the detector when the detectionconﬁdence is high or the tracking is considered fail. Due to the limited computational power on most MAV platforms, algorithms are implemented at two separated processing units.The detector runs at a ground control station (GCS) equipped with NVIDIA GTX 1060 while the tracker runs at a MAVonboard low-cost CPU. The transmission of image and target pose information is bridged via a high-speed Wi-Fi network to minimize the latency. In our experiment, the proposed framework is able to realize real-time detection and tracking with 30 frames per second (FPS) on our system.

# Summary. An optional shortened abstract.
summary: 
tags:
# - Source Themes 
featured: true

links:
# - name: Custom Link
#   url: http://example.org
url_pdf:  
url_code:  
url_dataset:  
url_poster:  
url_project: 
url_slides:  
url_source:  
url_video:  https://www.youtube.com/watch?v=kSz1FB7mgqU

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption:  
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
 

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides:  
---
 



