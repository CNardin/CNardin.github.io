---
title: "Bay-Fi preprint / working paper"
authors: ["Chiara Nardin", "Stefano Zorzi", "Federica Zonzini", "Oreste S. Bursi", "Daniele Zonta", "Marco Broccardo"]
show_author_list: false
date: "2025-10-07T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2025-10-08T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "EVACES25: Bay-Fi presentation"
publication_short: "Bay-Fi"

abstract: A Bayesian approach for main Frequency Identification on extremely undersampled signals

# Summary. An optional shortened abstract.
summary: A Bayesian approach for main Frequency Identification on extremely undersampled signals.

tags:
- system identification
- bay-fi
- bayesian

featured: true

hugoblox:
  ids:
    arxiv: https://ssrn.com/abstract=5863329

links:
- type: preprint
  provider: ssrn
  id: https://ssrn.com/abstract=5863329
- type: code
  url: https://github.com/CNardin
#- type: slides
#  url: https://www.slideshare.net/
#- type: dataset
#  url: "#"
#- type: poster
#  url: "#"
#- type: source
#  url: "#"
#- type: video
#  url: https://youtube.com
#- type: custom
#  label: Custom Link
#  url: http://example.org

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image: 
  filename: evaces-screen.png
  caption: conference #'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: ["bayfi"]
#- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

> [!ABSTRACT]
> Structural Health Monitoring (SHM) is gaining a key role in ensuring the integrity and safety of civil infrastructures. In the last decades, the rapid shift to wireless sensor networks has given rise to new challenges, mainly related to the limitation of data transmission and payloads, energy autonomy, and computing power needed for extracting useful information. To tackle these issues in the framework of vibration assessment, diverse algorithms have been proposed, mainly inspired by the compressed sensing theory, taking advantage of their inherent sparse nature as a set of multiple exponentially damped sinusoids. However, those solutions usually entail a signal reconstruction step, which is computationally expensive, and demonstrated scarce real-field effectiveness due to significant limitations in the maximum achievable compression ratio. Instead, in this work, we bypass these constraints by proposing an alternative method, termed Bayesian Frequency Identification (BAYFI), aimed at the identification of the main vibration frequency avoiding the decoding stage. The methodology is wrapped in a Bayesian formulation of an optimized, curve-fitting algorithm applied to random and extremely under-sampled measurement signal. BAY-FI is validated on a laboratory-scale, simply-supported beam and compared with conventional techniques, demonstrating significantly higher compression ratios while taking into consideration the importance of the sensor positioning.

> [!TIP]
> Click the *Cite* button above to copy *.bib* publication metadata into your notes.  
> or directly download here either the bibtex version:
> <a href="/papers/2025-EVACES-bayfi.bib" target="_blank">Download BibTeX</a>
> or the plain text one:
> <a href="/papers/2025-EVACES-bayfi.txt" target="_blank">Download Plain.txt</a>

<div class="scite-badge"
     data-doi="doi.org/10.1007/978-3-031-96114-4_53"
     data-layout="horizontal"
     data-show-zero="false"
     data-small="false"
     data-show-labels="true"
     data-tally-show="true">
</div>
<script async type="application/javascript" src="https://cdn.scite.ai/badge/scite-badge-latest.min.js">
</script>
