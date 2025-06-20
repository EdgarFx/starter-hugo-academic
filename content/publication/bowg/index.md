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

abstract: "Loop closure is critical in Simultaneous Localization and Mapping (SLAM) systems to reduce accumulative drift and ensure global mapping consistency. However, conventional methods struggle in perceptually aliased environments, such as narrow pipes, due to vector quantization, feature sparsity, and repetitive textures, while existing solutions often incur high computational costs. This paper presents Bag-of-Word-Groups (BoWG), a novel loop closure detection method that achieves superior precision-recall, robustness, and computational efficiency. The core innovation lies in the introduction of word groups, which captures the spatial co-occurrence and proximity of visual words to construct an online dictionary. Additionally, drawing inspiration from probabilistic transition models, we incorporate temporal consistency directly into similarity computation with an adaptive scheme, substantially improving precision-recall performance. The method is further strengthened by a feature distribution analysis module and dedicated post-verification mechanisms. To evaluate the effectiveness of our method, we conduct experiments on both public datasets and a confined-pipe dataset we constructed. Results demonstrate that BoWG surpasses state-of-the-art methods—including both traditional and learning-based approaches—in terms of precision-recall and computational efficiency. Our approach also exhibits excellent scalability, achieving an average processing time of 16 ms per image across 17,565 images in the Bicocca25b dataset. The source code is available at: https://github.com/EdgarFx/BoWG."
# Summary. An optional shortened abstract.
summary: ' '

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: 'https://github.com/EdgarFx/BoWG'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

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
