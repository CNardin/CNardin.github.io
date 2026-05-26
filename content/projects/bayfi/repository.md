---
title: Code Repository
description: This page provides access to the code repository associated with the Bay-Fi project, including links to the GitHub repository with source code and documentation.
date: 2025-10-27
weight: 4

toc: true
build:
  list: local
  render: always
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

## <i class="fa-brands fa-github"></i> Bay-Fi

The Bay-Fi source code is openly available on GitHub under the **MIT license**.

| | | | |
| :- | :- | :- | :- |
| [![GitHub](https://img.shields.io/badge/Source-GitHub-181717?logo=github)](https://github.com/CNardin/Bay-Fi) | ![License](https://img.shields.io/badge/License-MIT-blue) | ![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white) | ![Topics](https://img.shields.io/badge/SHM-Bayesian-green) |

> Bay-Fi is a Bayesian framework for extracting main vibration frequencies from extremely sparse, under-sampled signals — without requiring signal reconstruction or parameter tuning. It achieves higher compression ratios than traditional compressed sensing approaches.

### Repository Structure

| Folder | Description |
| :----- | :---------- |
| `BayFi/` | Core algorithm — `LIB.py` main library |
| `Classic-CS/` | MATLAB routines for convex optimization (comparison baseline) |
| `Examples/` | Application examples including a simply supported beam dataset |
| `Plotting/` | Visualization scripts |
| `Papers/` | Related conference and journal papers |
| `methodology.pdf` | Visual documentation of the Bayesian framework |

### Dependencies

```
numpy · scipy · tqdm · pyswarms
```
Python 3.13 — install via `pip install -r requirements.txt`

### Authors

Chiara Nardin · Stefano Zorzi · Federica Zonzini · Marco Broccardo

:bulb: Star the repo on [GitHub](https://github.com/CNardin/Bay-Fi) to follow updates!
