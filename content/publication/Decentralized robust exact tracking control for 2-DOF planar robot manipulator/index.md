---
title: "Decentralized robust exact tracking control for 2-DOF planar robot manipulator"
authors:
- Zhenxing Sun
- nico # put this author name instead of your name directly will enable the function of showing your Info at the end of the publication page
- Xinghua Zhang
- Haoyong Yu 
date: "2018-06-01T21:44:14+08:00"
doi: ""
draft: true
# Schedule page publish date (NOT publication's date).
publishDate: "2018-06-01T21:44:14+08:00"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In *International Conference on Advanced Robotics and Mechatronics (ICARM)*, IEEE
publication_short:  In *ICARM*

abstract: In this study, a novel decentralized exact tracking control approach for 2-DOF planar robot manipulators with disturbances and uncertainties has been proposed. The main idea of the proposed method is to partition the whole robot manipulator into single joint and lumped disturbance. A well designed extended high gain observer (EHGO) is adopted to observe the lumped disturbance of each joint, which includes coupling, load disturbance and uncertainty, etc. Rather than coping with the robot manipulator as a whole, the proposed method is locally designed to compensate the estimated coupling and stabilize the internal states of a single joint. By doing that, each joint can be virtually decoupled from the whole robot manipulator and functions in a relatively independent way. When joints are interconnected, the stabilization of the whole robot manipulator would be obtained by only guaranteeing the localized stability of individual joint. The theoretical analyses are rigorously conducted by utilizing Lyapunov stability theorem. Simulation results illustrate the effectiveness of the proposed control scheme.

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
url_video:  

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
 