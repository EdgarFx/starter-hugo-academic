---
title: 'Power System Fault Diagnosis with Quantum Computing and Efficient Gate Decomposition'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Admin
  - Huan Zhao
  - Xiyuan Zhou
  - Junhua Zhao
  - Ting Shu
  - Fushuan Wen

# Author notes (optional)
# author_notes:
#   - ''
#   - ''
#   - ''
#   - ''


date: '2023-04-15T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2023-04-15T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['2']

# Publication name and optional abbreviated publication name.
publication: Applied Energy (Under Review)
# publication_short: In *JFR*

abstract: Power system fault diagnosis is crucial for identifying the location and causes of the fault process and providing fault decision-making basis for the dispatchers. However, classical methods suffer from significant time-consuming, memory overhead, and computational complexity issues as the scale of system increases. With the rapid development of quantum computing technology, the combinatorial optimization solution method based on quantum computing has shown certain advantages in computational time. Therefore, this paper proposes a quantum computing based power system fault diagnosis method with Quantum Approximate Optimization Algorithm (QAOA). The proposed method uses the Ising model to construct the problem Hamiltonian, which completely preserves the coupling relationship between the faulty components and the various operations of protective relays (PR) and circuit breakers (CB). Additionally, the symmetric equivalent decomposition of the multi-z-rotation gate is proposed to enhance the problem-solving efficiency under current equipment limitations. Furthermore, a method to reduce the number of qubits required by quantum computing is proposed, which utilizes the small probability events characteristic of the power system. The simulation results based on a test system show that proposed methods can achieve the same optimal results and have a faster speed than the classical algorithm.
# Summary. An optional shortened abstract.
summary: ''

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
# image:
#   caption: 'Image credit: [**Zhouyang**](https://www.researchgate.net/profile/Zhou-Yang-18/research)'
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
research:
  - q_optimization

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
#slides: example
---
