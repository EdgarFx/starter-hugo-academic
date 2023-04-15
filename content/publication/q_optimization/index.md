---
title: 'Quantum Computing Based Power System Fault Diagnosis with QAOA and Efficient Gate Decomposition'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Admin
  - Huan Zhao
  - Junhua Zhao

# Author notes (optional)
# author_notes:
#   - ''
#   - ''
#   - ''
#   - ''


date: ''
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: ''

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
# publication: In *JFR 2022*
# publication_short: In *JFR*

abstract: Power system fault diagnosis helps to reproduce the fault process and provide the dispatchers with a basis for fault decision-making. However, classical methods suffer from significant time-consuming, memory overhead, and computational complexity issues, especially in the case of many grid devices and large scales. Nowadays, with the continuous development of quantum computing, the optimal solution method based on quantum computing is expected to solve this problem. This paper proposes a power system fault diagnosis method based on Quantum Approximate Optimization Algorithm (QAOA) for the first time. The proposed method uses the Ising model to construct the problem Hamiltonian, which completely preserves the coupling relationship between the faulty components and the operation of PR and CB, and considers the failed/mal operation of PR and CB, as well as the wrong alarm. In addition, this paper proposes the symmetric equivalent decomposition of the multi-z-rotation gate, which can efficiently solve the PUBO problem under the current equipment limitations using QAOA. The paper also reduces the required number of qubits through the small probability events characteristic of the power system. Case studies based on an example system were conducted, which demonstrate the effectiveness of the proposed method. Moreover, experiments show that the quantum algorithm may have a faster speed than the classical algorithm.
# Summary. An optional shortened abstract.
summary: QAOA-based power system fault diagnosis with proposed efficient quantum gate decomposition.

tags: []

# Display this page in the Featured widget?
featured: false

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
# image:
#   caption: 'Image credit: [**Zhouyang**](https://www.researchgate.net/profile/Zhou-Yang-18/research)'
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# research:
#   - construction_robot

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---
