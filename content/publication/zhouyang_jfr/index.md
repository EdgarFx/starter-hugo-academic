---
title: 'Building information modeling‐based 3D reconstruction and coverage planning enabled automatic painting of interior walls using a novel painting robot in construction'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Yang Zhou
  - Peng Li
  - Zefeng Ye
  - admin
  - Linhai Gui
  - Jiang Xin
  - Xiang Li
  - Yunhui Liu

# Author notes (optional)
author_notes:
  - ''
  - ''
  - ''
  - 'Hardware and partial control framework(RA Work)'


date: '2022-06-21T00:00:00Z'
doi: 'https://doi.org/10.1002/rob.22103'

# Schedule page publish date (NOT publication's date).
publishDate: '2022-06-21T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: In *JFR 2022*
publication_short: In *JFR*

abstract: Due to the lack of experienced labor and high-quality requirements, interior painting task calls for robotic solutions in the construction field. This paper presents a robotic system aiming for the automatic interior wall painting task. The new painting robot comprises an omnidirectional mobile base and a seven degrees-of-freedom (7-DOF) redundant manipulator consisting of a 6-DOF robot arm and a 1-DOF lifting mechanism to make the painting task more flexible. Further, a building information modeling-based three-dimensional (3D) reconstruction approach is used to obtain the complete 3D model of all walls in the interior environment for automatic painting. Moreover, we propose a two-stage coverage planning framework to automatically generate optimal mobile base paths and manipulator trajectories to paint the walls. In the proposed framework, the global planner plans the painting waypoints sequence optimally. The local planner generates the mobile base poses by a new evaluation function which both ensures coverage of all painting waypoints and optimizes robot paths length. The results of field tests showed that the whole painting robot system has high environment adaptability to paint interior walls automatically. Furthermore, the planning results can significantly reduce total robot paths length compared with the previous studies. The painting robot can automatically finish a painting of 46.3 square meter in 59.3 mins, and this performance verifies the proposed design and algorithms.
# Summary. An optional shortened abstract.
summary: Painting Robot

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://onlinelibrary.wiley.com/doi/full/10.1002/rob.22103'
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
  caption: 'Image credit: [**Zhouyang**](https://www.researchgate.net/profile/Zhou-Yang-18/research)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
research:
  - construction_robot

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---
