---
title: 'Bag of Word Groups (BoWG): A Robust and Efficient Loop Closure Detection Method Under Perceptual Aliasing'
summary: A definition of word groups exploiting the co-occurrence and proximity of visual words. This representation enriches the discriminative information of images with similar appearance; An online word group database is designed and implemented, providing context-specific representation. Through the integration of direct and inverse index tables, our system achieves efficient loop closure detection suitable for large-scale applications; Temporal consistency and feature distribution information are incorporated directly into the similarity score calculation, complemented by dedicated temporal and geometrical post-verification modules. These additions further improve the system’s precision and recall.

tags:
  - Computer Vision and Robotics

date: '2025-06-15T00:00:00Z'

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
url_code: 'https://github.com/EdgarFx/BoWG'
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

Loop closure is critical in Simultaneous Localization and Mapping (SLAM) systems to reduce accumulative drift and ensure global mapping consistency. However, conventional methods struggle in perceptually aliased environments, such as narrow pipes, due to vector quantization, feature sparsity, and repetitive textures, while existing solutions often incur high computational costs. This paper presents Bag-of-Word-Groups (BoWG), a novel loop closure detection method that achieves superior precision-recall, robustness, and computational efficiency. The core innovation lies in the introduction of word groups, which captures the spatial co-occurrence and proximity of visual words to construct an online dictionary. Additionally, drawing inspiration from probabilistic transition models, we incorporate temporal consistency directly into similarity computation with an adaptive scheme, substantially improving precision-recall performance. The method is further strengthened by a feature distribution analysis module and dedicated post-verification mechanisms. To evaluate the effectiveness of our method, we conduct experiments on both public datasets and a confined-pipe dataset we constructed. Results demonstrate that BoWG surpasses state-of-the-art methods—including both traditional and learning-based approaches—in terms of precision-recall and computational efficiency. Our approach also exhibits excellent scalability, achieving an average processing time of 16 ms per image across 17,565 images in the Bicocca25b dataset. The source code is available at: https://github.com/EdgarFx/BoWG.