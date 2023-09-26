---
title: Bag-of-Word-Groups (BoWG), A Robust Loop Closure Module for In-pipe Visual-Laser-Inertial SLAM
summary: A feature detector capable of detecting features at different scales based on an image pyramid. A definition of word groups exploiting the spatial co-occurrence of detected features, which provides context-specific feature representation. A database is established and updated online storing the word group information of each image, which enables efficient loop closure score computation.

tags:
  - Computer Vision and Robotics

date: '2023-08-04T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

# image:
#   caption: Photo by linzhu on HK
#   focal_point: Smart

# links:
#   - icon: zhihu
#     icon_pack: fab
#     name: Follow
#     url: https://www.zhihu.com/people/yuexiaozhu
url_code: ''
url_pdf: ''
url_slides: 'https://docs.google.com/presentation/d/1maY7paywcalkHGTucG-XSmBUghmM3jYc/edit?usp=sharing&ouid=110083063639360259216&rtpof=true&sd=true'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

In-pipe simultaneous localization and mapping (SLAM) techniques with photorealistic RGB-D reconstruction capability have the potential to enhance human labor to inspect pipe conditions and localize anomalies, thereby preventing hazardous leaks and explosions. Loop closure detection is vital in the process of SLAM, as it helps reduce the accumulative drift of the robot’s estimated odometry and generate a globally consistent map. However, in confined-space environments such as narrow pipes, conventional loop closure methods suffer perceptual aliasing due to feature scarcity and textural repetitiveness. In this research, we aim to develop a robust loop closure module in confined-space environments on top of our prior confined-space dense RGB-D SLAM method, visual-laser-inertial (VLI) SLAM. Specifically, we define the concept of word group based on spatial proximity and positions of features and propose to build and maintain a novel loop closure detection module called Bag-of-Word-Groups (BoWG) online, which provides context-specific feature representation. Besides, we utilize Gaussian pyramids to implement Multi-scale Good Features To Track (MS-GFTT) to detect richer features at various scales for word group analysis. Our method does not require any extra sensor other than a monocular visual camera and can be easily integrated into existing Bag-of-Words (BoW) methods. To validate the proposed method, we conduct real-world experiments in a narrow, feature-sparse pipeline with loops. Experiment results show that our method is robust and can achieve high precision while maintaining acceptable recall when the perceptual aliasing problem is serious. In addition, the proposed method has the potential to be applied to environments other than narrow pipes.