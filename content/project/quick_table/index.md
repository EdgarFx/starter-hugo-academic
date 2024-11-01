---
title: QuickTable, an ultra lightweight application to extract tables in PDF
summary: proposes a new pipeline to extract tables of interest in PDF files, and develops an ultra lightweight application named QuickTable accordingly.

date: '2022-08-20T10:00:00Z'

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
url_code: 'https://github.com/EdgarFx/QuickTable'
url_pdf: 'https://edgarfx.github.io/uploads/quick_table.pdf'
url_slides: 'https://docs.google.com/presentation/d/1Trhs2e3a0LPJ0MgIhHpDXLulBNFTcZUI/edit?usp=sharing&ouid=110083063639360259216&rtpof=true&sd=true'
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

This research proposes a new pipeline to extract tables of interest in PDF files, and develops an ultra lightweight application named QuickTable accordingly. Most of the previous research only focused on one or two tasks of table recognition and there is little research on finding tables of interest. The developed QuickTable uses the proposed pipeline based on PP-Picodet, SLANet, PPOCRv3, Text Segmentation and Cosine Similarity Analysis, which allows users to upload PDF files **from mobile devices** and **enter keywords to get tables of interest**. In addition, we have trained models in both Chinese and English so that users can upload files in **different languages**. Experiments show that the proposed pipeline is lightweight and outperforms previous approaches, demonstrating the effectiveness of our method. The [code](https://github.com/EdgarFx/QuickTable) is open-sourced.