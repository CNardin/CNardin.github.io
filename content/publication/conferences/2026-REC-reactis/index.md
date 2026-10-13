---
title: "A continuous-time Markovian framework for performance-based earthquake engineering: integrated seismic risk and resilience assessment"
authors: ["chiara-nardin", "stefano-marelli", "bruno-sudret", "marco-broccardo"]
show_author_list: false
date: "2026-08-01T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2026-08-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "*REC 2026 – 11th International Workshop on Reliable Engineering Computing: Reliability Computations in a Data and Model-Driven World*, TU Dortmund University, TUDObooks, pp. 495–506"
publication_short: ""

abstract: "Assessing the seismic reliability of structural systems increasingly requires models that jointly represent damage evolution and recovery. Yet, the traditional PEER PBEE formulation does not capture the temporal dynamics of post-event repair, and modern reliability analyses often rely on scarce or uncertain recovery data, motivating the need for tractable methods. We reformulate the PEER PBEE framework using a continuous time Markov Chain (CTMC) Monte Carlo approach, which naturally models probabilistic transitions among damage and recovery states under time-invariant seismic hazards. Transition rates incorporate metamodel-based state-dependent fragility functions, as well as recovery processes, yielding a unified representation of hazard effects and system evolution. Leveraging the analytical properties of CTMCs, we compute steady-state performance statistics, such as mean time to failure and time spent in degraded states, and define a resilience index adapted from the classical reliability index β. The approach is tested on a simple yet representative example, showing that the CTMC-enhanced PBEE framework captures the temporal progression from damage to recovery in a computationally efficient and data-flexible manner."

# Summary. An optional shortened abstract.
summary: "A continuous-time Markov chain (CTMC) reformulation of the PEER PBEE framework that jointly models damage and recovery, yielding steady-state performance statistics and a resilience index."

tags:
- reactis
- PEER PBEE framework
- seismic reliability
- recovery
- CTMC
- resilience

featured: false

links:
  - type: pdf
    url: /papers/2026-REC-reactis.pdf
  - type: publisher
    url: https://doi.org/10.17877/tudobooks-11.159
  - type: project
    url: /projects/reactis/
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
  filename: featured.png
  caption: "State transition diagram of the CTMC model and sample damage-state trajectories (from the paper)"
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: ["reactis"]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

> [!ABSTRACT]
> Assessing the seismic reliability of structural systems increasingly requires models that jointly represent damage evolution and recovery. Yet, the traditional PEER PBEE formulation does not capture the temporal dynamics of post-event repair, and modern reliability analyses often rely on scarce or uncertain recovery data, motivating the need for tractable methods. We reformulate the PEER PBEE framework using a continuous time Markov Chain (CTMC) Monte Carlo approach, which naturally models probabilistic transitions among damage and recovery states under time-invariant seismic hazards. Transition rates incorporate metamodel-based state-dependent fragility functions, as well as recovery processes, yielding a unified representation of hazard effects and system evolution. Leveraging the analytical properties of CTMCs, we compute steady-state performance statistics, such as mean time to failure and time spent in degraded states, and define a resilience index adapted from the classical reliability index β. The approach is tested on a simple yet representative example, showing that the CTMC-enhanced PBEE framework captures the temporal progression from damage to recovery in a computationally efficient and data-flexible manner.

> [!TIP]
> Click the *Cite* button above to copy *.bib* publication metadata into your notes.
> or directly download here either the bibtex version:
> <a href="/papers/2026-REC-reactis.bib" target="_blank">Download BibTeX</a>
> or the plain text one:
> <a href="/papers/2026-REC-reactis.txt" target="_blank">Download Plain.txt</a>

<div class="scite-badge"
     data-doi="doi.org/10.17877/tudobooks-11.159"
     data-layout="horizontal"
     data-show-zero="false"
     data-small="false"
     data-show-labels="true"
     data-tally-show="true">
</div>
<script async type="application/javascript" src="https://cdn.scite.ai/badge/scite-badge-latest.min.js">
</script>
