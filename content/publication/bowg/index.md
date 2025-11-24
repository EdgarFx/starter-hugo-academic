---
title: "Bag of Word Groups (BoWG): A Robust and Efficient Loop Closure Detection Method Under Perceptual Aliasing"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Admin
  - Tina Tian
  - Howie Choset
  - Lu Li
# Author notes (optional)
# author_notes:
#   - 'Equal contribution'
#   - 'Equal contribution'


date: '2025-06-15T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2025-06-15T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS) 2025
# publication_short: IROS 2025

# abstract: "Loop closure is critical in Simultaneous Localization and Mapping (SLAM) systems to reduce accumulative drift and ensure global mapping consistency. However, conventional methods struggle in perceptually aliased environments, such as narrow pipes, due to vector quantization, feature sparsity, and repetitive textures, while existing solutions often incur high computational costs. This paper presents Bag-of-Word-Groups (BoWG), a novel loop closure detection method that achieves superior precision-recall, robustness, and computational efficiency. The core innovation lies in the introduction of word groups, which captures the spatial co-occurrence and proximity of visual words to construct an online dictionary. Additionally, drawing inspiration from probabilistic transition models, we incorporate temporal consistency directly into similarity computation with an adaptive scheme, substantially improving precision-recall performance. The method is further strengthened by a feature distribution analysis module and dedicated post-verification mechanisms. To evaluate the effectiveness of our method, we conduct experiments on both public datasets and a confined-pipe dataset we constructed. Results demonstrate that BoWG surpasses state-of-the-art methods—including both traditional and learning-based approaches—in terms of precision-recall and computational efficiency. Our approach also exhibits excellent scalability, achieving an average processing time of 16 ms per image across 17,565 images in the Bicocca25b dataset. The source code is available at: https://github.com/EdgarFx/BoWG."
# # Summary. An optional shortened abstract.
summary: ' '

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://arxiv.org/abs/2510.22529'
url_code: 'https://github.com/EdgarFx/BoWG'
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
  - bowg

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---

## Overview
This paper presents Bag-of-Word-Groups (BoWG), a novel loop closure detection method that achieves superior precision-recall, robustness, and computational efficiency. The core innovation lies in the introduction of word groups, which captures the spatial co-occurrence and proximity of visual words to construct an online dictionary. Additionally, drawing inspiration from probabilistic transition models, we incorporate temporal consistency directly into similarity computation with an adaptive scheme, substantially improving precision-recall performance. The method is further strengthened by a feature distribution analysis module and dedicated post-verification mechanisms.


<div style="margin: 2rem 0;">
  <h2>Loop Closure Detection Using BoWG on New College</h2>
  <img src="nc_demo.gif" alt="NC Demo" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>BoWG vs DBoW2</h2>
  <img src="demo.gif" alt="BoWG vs DBoW2" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Performance Compared With Exising Methods</h2>
  <img src="results.png" alt="Performance Compared With Exising Methods" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Performance on a More Challenging Pipe Environment</h2>
  <div style="display: flex; gap: 20px;">
    <img src="test_site.png" alt="Test Site" style="width: 40%; object-fit: contain; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <img src="A_Res.png" alt="Results" style="width: 60%; object-fit: contain; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
  </div>
</div>

<div style="margin: 2rem 0;">
  <h2>Integrate BoWG into VINS-Mono</h2>
  <img src="MH03_vins_bowg.gif" alt="Integrate BoWG into VINS-Mono" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
</div>

<div style="margin: 2rem 0;">
  <h2>Video</h2>
  <video width="100%" controls style="border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <source src="video.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

<!-- <video width="100%" controls>
  <source src="demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


![BoWG vs DBoW2](demo.gif) -->
