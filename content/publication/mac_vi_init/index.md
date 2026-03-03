---
title: "MAC-I²: Learned Metrics-Aware Covariance for Robust Visual-Inertial Initialization and Calibration"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Admin
  - Yuheng Qiu
  - Yutian Chen
  - Ruogu Li
  - Can Xu
  - Sebastian Scherer
# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'


date: '2025-11-24T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2025-11-24T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: Submitted to Robotics Science and Systems (RSS) 2026
# publication_short: RSS 2026

summary: ' '

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ''
  focal_point: ''
  preview_only: true

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
research:
  - mac_vi_init

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---

## Overview
Visual-inertial (VI) initialization and calibration are critical for the performance of VI systems, as they provide camera-IMU extrinsics and physically consistent initial state estimates for sensor fusion. However, traditional methods rely heavily on geometric feature correspondences and often struggle in challenging environments involving illumination changes, dynamic objects, and occlusions. In this paper, we present MAC-I$^2$, a robust VI initialization and online calibration framework that leverages learning-based visual features and uncertainty modeling. Specifically, we derive visual pose covariances from learned feature-matching uncertainties and adopt a learning-based IMU model to predict IMU integration covariances. Both visual and inertial covariances are metrics-aware, enabling principled and tuning-free VI initialization and calibration. Extensive experiments demonstrate that MAC-I$^2$ achieves significantly improved robustness and accuracy across a wide range of challenging scenarios where geometry-based methods often fail.

<!-- ## Video Demos
These videos illustrate the gravity-direction initialization results (Orange: estimated gravity; Green: ground truth) across different environments. Subsequent localization and mapping are carried out by jointly optimizing the visual pose graph (PGO) together with either standard IMU residuals or those from AirIMU. When AirIMU is used, the localization and mapping system effectively becomes **MACVIO**, a learning-based stereo visual-inertial odometry that we are also developing.

<div style="margin: 2rem 0;">
  <h3>Lunar Environment (TartanairV2 Dataset)</h3>
  <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="lunar.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>


<div style="display: flex; gap: 1rem; margin: 2rem 0;">
  <div style="flex: 1;">
    <h3>VBR Colosseo Train 0 (Extreme Exposure)</h3>
    <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <source src="vbr_light.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  
  <div style="flex: 1;">
    <h3>VBR Colosseo Train 0 (Dynamic Scene)</h3>
    <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <source src="vbr_dynamic.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div style="display: flex; gap: 1rem; margin: 2rem 0;">
  <div style="flex: 1;">
    <h3>EuRoC V102</h3>
    <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <source src="V102.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
  
  <div style="flex: 1;">
    <h3>EuRoC V203</h3>
    <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
      <source src="V203.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div style="margin: 2rem 0;">
  <h2>Successful Initialization Comparison on V102 Sequence of EuRoC Dataset</h2>
  <img src="success.png" alt="success" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Performance Comparison on EuRoC Dataset (SR in the table refers to the success rate)</h2>
  <img src="results_euroc.png" alt="euroc_init" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Performance of the proposed MAC-VI-Init on TUM and VBR Dataset</h2>
  <img src="results_tum_vbr.png" alt="tum_vbr_init" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Gyroscope Bias Estimation Comparison on EuRoC Dataset</h2>
  <img src="gyro_bias.png" alt="gyro_bias" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Pose Covariance Analysis on TartanAir Dataset</h2>
  <div style="display: flex; flex-direction: column; gap: 5px;">
    <img src="pose_cov_bin.png" alt="Test Site" style="width: 100%; display: block; object-fit: contain; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <img src="pose_cov_trans.png" alt="Results" style="width: 100%; display: block; object-fit: contain; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <img src="pose_cov_rot.png" alt="Third Image" style="width: 100%; display: block; object-fit: contain; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  </div>
</div> -->