---
title: "DeformX: A Versatile Co-Simulation Framework for Deformable Linear Objects"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Yi Yang
  - Admin
  - Lehong Wang
  - Chenghao Li
  - Zilin Dai
  - Henry Kou
  - Lu Li
  - Howie Choset
# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'
  - 'Equal contribution'


date: '2026-03-02T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2026-03-02T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: Submitted to IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS) 2026
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
  - deformx

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---

## Overview
Deformable linear objects (DLOs) such as wires, cables, and ropes are common in robotic manipulation tasks, yet simulating them with both visual realism and physical accuracy remains challenging. Existing visual simulation methods typically rely on procedural geometric primitives that lack physically grounded deformation behavior, while physics-based approaches with robot learning support often approximate DLOs as rigid-link chains or generic soft bodies, failing to accurately capture the bending, twisting, and shear mechanics of slender elastic structures. In this work, we introduce DeformX, a co-simulation framework that integrates a dedicated Cosserat rod physics engine with NVIDIA Isaac Sim, enabling DLO simulations that are both physically faithful and visually realistic. Our Cosserat rod engine simulates the dynamics and self-collisions of DLOs, and contact interactions with arbitrary free-form meshes. To achieve high-fidelity visualization, we employ mesh skinning to map discrete rod deformations onto imported CAD models. To the best of our knowledge, DeformX is the first framework for DLO simulation that unifies realistic visualization, principled physics, and compatibility with robot learning pipelines. We demonstrate its versatility across synthetic data generation and policy learning for DLO manipulation, and validate visual and physical fidelity through comparisons against real-world experiments. Notably, fine-tuning Segment Anything Model 3 (SAM3) on DeformX-generated data yields a 10.2\% mAP@75 improvement in real-image wire segmentation, and a rope-swinging policy trained entirely in DeformX achieves a mean target-hitting error of 6.6 cm on a UR5e manipulator in real-world trials, highlighting its strong sim-to-real transfer capability.

## Demo Video

<div class="video-embed">
  <h3>Introducing DeformX, a versatile co-simulation framework for deformable linear objects</h3>
  <div class="video-embed__frame">
    <video controls>
      <source src="demo.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>


<div class="video-grid">
  <div class="video-grid__col">
    <h3>Hit Apple Demo 1</h3>
    <div class="video-embed__frame">
      <video controls>
        <source src="apple1.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </div>
  
  <div class="video-grid__col">
    <h3>Hit Apple Demo 2</h3>
    <div class="video-embed__frame">
      <video controls>
        <source src="apple2.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </div>
</div>
