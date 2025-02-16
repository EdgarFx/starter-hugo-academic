<!-- ---
title: SLAM for Vision-based Navigation
summary: Integration of learning-based perception techniques and visual SLAM methods to develop a reliable and efficient autonomous navigation system that can adapt to challenging and unpredictable scenarios with a high success rate.

date: '2023-05-20T10:00:00Z'

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
url_pdf: 'https://edgarfx.github.io/uploads/navigation_report.pdf'
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

This research project is initiated by Prof. Shankar Sastry (UC Berkeley) and Prof. Somil Bansal (University of Southern California). The main aim of the research is to create a new autonomous navigation pipeline that incorporates learning-based perception for extracting distinctive features and semantic interpretation, and model-based SLAM for inference and metric map reconstruction. 

Specifically, learning-based perception techniques have the ability to successfully identify objects that are important for the subsequent navigation task, but may face difficulties in accurately reconstructing metrics in challenging scenarios such as narrow hallways and tight corners. On the other hand, visual SLAM methods can produce consistent metric maps but often require significant computational resources, and do not provide relevant semantic information. This study aims to explore methods of integrating these two approaches, learning-based and model-based, to establish an efficient and reliable autonomous navigation system that can achieve high success rates and adapt to complex and unpredictable environments.

I was honored to directly mentored by Dr. Chih-Yuan Chiu and Prof. Somil Bansal in this project. Our work was based on Prof. Bansal's prior work [LB-WayPtNav](https://smlbansal.github.io/LB-WayPtNav/), which is a learning-based navigation method and can generate some way points to guide the movement of the robot. This method can be used to navigate in novel environments, however, it would generate infeasible paths for some cases such as tight corners and narrow hallways. This is because this method struggles to provide accurate metric reconstruction when necessary (e.g. tight corners, narrow hallways). Meanwhile, visual SLAM algorithms can generate consistent metric maps, but are often computationally expensive to run, and do not provide relevant semantic information. Therefore, we try to establish a pipeline that combines both SLAM and the learning-based method to support an efficient autonomous navigation framework. 

As a proof of concept, we showed that SLAM with particle filtering pairing algorithm and LiDAR information is able to successfully navigate situations that proved challenging for the purely learning based approach presented by Bansal. After that, we designed a switching mechanism that can switch to SLAM from learning based approach when the current scene is challenging, which is based on [reachability analysis](https://arxiv.org/abs/2211.02736). -->