---
title: "Bag-of-Word-Groups (BoWG): A Robust Loop Closure Module for In-pipe Visual-Laser-Inertial SLAM"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Admin
  - Tina Tian
  - Lu Li
  - Howie Choset
# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'


date: '2023-08-04T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2023-08-04T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: Carnegie Mellon Robotics Institute Summer Scholars Working Papers Journal 2023
# publication_short: In *IROS*

abstract: In-pipe simultaneous localization and mapping (SLAM) techniques with photorealistic RGB-D reconstruction capability have the potential to enhance human labor to inspect pipe conditions and localize anomalies, thereby preventing hazardous leaks and explosions. Loop closure detection is vital in the process of SLAM, as it helps reduce the accumulative drift of the robot’s estimated odometry and generate a globally consistent map. However, in confined-space environments such as narrow pipes, conventional loop closure methods suffer perceptual aliasing due to feature scarcity and textural repetitiveness. In this research, we aim to develop a robust loop closure module in confined-space environments on top of our prior confined-space dense RGB-D SLAM method, visual-laser-inertial (VLI) SLAM. Specifically, we define the concept of word group based on spatial proximity and positions of features and propose to build and maintain a novel loop closure detection module called Bag-of-Word-Groups (BoWG) online, which provides context-specific feature representation. Besides, we utilize Gaussian pyramids to implement Multi-scale Good Features To Track (MS-GFTT) to detect richer features at various scales for word group analysis. Our method does not require any extra sensor other than a monocular visual camera and can be easily integrated into existing Bag-of-Words (BoW) methods. To validate the proposed method, we conduct real-world experiments in a narrow, feature-sparse pipeline with loops. Experiment results show that our method is robust and can achieve high precision while maintaining acceptable recall when the perceptual aliasing problem is serious. In addition, the proposed method has the potential to be applied to environments other than narrow pipes.
# Summary. An optional shortened abstract.
summary: false

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
url_poster: 'https://docs.google.com/presentation/d/1Fttcj0lzZ_AiARmjTG51l_Mxh_Jk9hSI/edit?usp=sharing&ouid=110083063639360259216&rtpof=true&sd=true'
url_project: ''
url_slides: 'https://docs.google.com/presentation/d/1maY7paywcalkHGTucG-XSmBUghmM3jYc/edit?usp=sharing&ouid=110083063639360259216&rtpof=true&sd=true'
url_source: ''
url_video: 'https://drive.google.com/file/d/1spFpAk-oNTidfoz4TQxxwRUvRthoZibf/view?usp=sharing'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# image:
#   caption: 'Image credit: [**Linzhu**](https://www.zhihu.com/people/yuexiaozhu)'
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
research:
  - bowg

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---
