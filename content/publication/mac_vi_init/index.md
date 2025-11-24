---
title: "MAC-VI-Init: Robust Visual-Inertial Initialization and Calibration with Learning-based Features and Uncertainty"

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
publishDate: '2026-07-13T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: (Working Paper) Preparing for Robotics Science and Systems (RSS) 2026
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
This paper presents MAC-VI-Init, a robust and accurate VI initialization and online calibration method. Traditional methods are struggled in challenging environments, such as severe illumination changes, dynamic objects, occlusions, and fast motions, due to the limitation of geometric visual features. Our method utilizes the learning-based feature matching and metrics-aware covariances to robustly estimate visual poses. In addition, the covariance of the estimated visual poses is also computed for better VI joint optimization. A learning-based IMU model can be further incorporated, which provides accurate IMU corrections and the uncertainty of IMU pre-integrations. Experiments on challenging scenarios demonstrate that our method significantly improves the robustness and accuracy of VI initialization and mapping.

