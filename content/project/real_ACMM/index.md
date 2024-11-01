---
title: Photorealistic-3D-Reconstruction-with-Multi-view-Stereo
summary: Multi-View Stereo with Broad Adaptive Checkerboard Sampling and Dynamic Multi-Hypothesis Joint View Selection, improvements based on ACMM

date: '2024-01-20T10:00:00Z'

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
url_code: 'https://github.com/EdgarFx/Photorealistic-3D-Reconstruction-with-Multi-view-Stereo'
url_pdf: 'https://edgarfx.github.io/uploads/real_ACMM.pdf'
url_slides: 'https://docs.google.com/presentation/d/1b5vOJpfoab8EPCnQ__-Rmh4ZOsqP7_7_/edit?usp=sharing&ouid=110083063639360259216&rtpof=true&sd=true'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

In this research project, we propose real-ACMM, which is a photorealistic 3D reconstruction method with MVS. The proposed real-ACMM is based on the architecture of [ACMM](https://arxiv.org/abs/1904.08103), and we make improvements on ACMM, achieving better reconstruction results with fewer iterations, especially in low-texture areas. The [code](https://github.com/EdgarFx/Photorealistic-3D-Reconstruction-with-Multi-view-Stereo) is open-sourced.

Our main contributions are:
* Proposed Broad Adaptive Checkerboard Sampling, which broadly considers all the pixels in a neighborhood window during pixel sampling, instead of extending in a specific direction. This method helps capture correct hypotheses in large low-texture areas.
* Introduced Dynamic Multi-Hypothesis Joint View Selection, which dynamically adjusts the matching cost for both the good matching and bad matching, allowing more robust and accurate view selection.
* Results show that the proposed method can achieve better reconstruction results with fewer iterations, especially in low-texture areas. 

## Results in ETH3D benchmark

![Depth map comparison between different algorithms on ETH3D pipes dataset](depth.png)

![Point cloud comparisons between different algorithms on ETH3D pipes dataset](point.png)