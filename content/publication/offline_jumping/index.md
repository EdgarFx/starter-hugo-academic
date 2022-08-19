---
title: 'An Optimal Motion Planning Framework for Quadruped Jumping'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - zhitao Song
  - admin
  - Guangli Sun
  - Hongsuo Wei
  - Yihu Ling
  - Linhai Gui
  - Yunhui Liu

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'


date: '2022-07-25T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2022-07-25T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: In *IROS 2022*
publication_short: In *IROS*

abstract: This paper presents an optimal motion planning framework to generate versatile energy-optimal quadrupedal jumping motions automatically (e.g., flips, spin). The jumping motions via the centroidal dynamics are formulated as a 12-dimensional black-box optimization problem subject to the robot kino-dynamic constraints. Gradient-based approaches offer great success in addressing trajectory optimization (TO), yet, prior knowledge (e.g., reference motion, contact schedule) is required and results in sub-optimal solutions. The new proposed framework first employed a heuristics-based optimization method to avoid these problems. Moreover, a prioritization fitness function is created for heuristics-based algorithms in robot ground reaction force (GRF) planning, enhancing convergence and searching performance considerably. Since heuristics-based algorithms often require significant time, motions are planned offline and stored as a pre-motion library. A selector is designed to automatically choose motions with user-specified or perception information as input. The proposed framework has been successfully validated only with a simple continuously tracking PD controller in an open-source Mini-Cheetah by several challenging jumping motions, including jumping over a window-shaped obstacle with 30 cm height and left-flipping over a rectangle obstacle with 27 cm height.
# Summary. An optional shortened abstract.
summary: Heuristic-based offline jumping framework

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/abs/2207.12002'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: 'https://www.youtube.com/watch?v=AJ37eS8sjS8&t=2s'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Linzhu**](https://www.zhihu.com/people/yuexiaozhu)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
research:
  - offline_quadruped_jumping

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---
