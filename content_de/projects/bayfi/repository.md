---
title: Code-Repository
description: Zugang zum Code-Repository des Projekts Bay-Fi, mit Links zum GitHub-Repository, zum Quellcode und zur Dokumentation.
date: 2025-10-27
weight: 4

toc: true
build:
  list: local
  render: always
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

## <i class="fa-brands fa-github"></i> Bay-Fi

Der Quellcode von Bay-Fi ist auf GitHub unter der **MIT-Lizenz** frei verfügbar.

| | | | |
| :- | :- | :- | :- |
| [![GitHub](https://img.shields.io/badge/Source-GitHub-181717?logo=github)](https://github.com/CNardin/Bay-Fi) | ![License](https://img.shields.io/badge/License-MIT-blue) | ![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white) | ![Topics](https://img.shields.io/badge/SHM-Bayesian-green) |

> Bay-Fi ist ein bayessches Framework, um die wichtigsten Schwingungsfrequenzen aus extrem spärlichen, unterabgetasteten Signalen zu bestimmen, ohne Signalrekonstruktion und ohne Parameterabstimmung. Es erreicht höhere Kompressionsraten als klassische Compressed-Sensing-Verfahren.

### Aufbau des Repositorys

| Ordner | Beschreibung |
| :----- | :---------- |
| `BayFi/` | Kernalgorithmus: Hauptbibliothek `LIB.py` |
| `Classic-CS/` | MATLAB-Routinen zur konvexen Optimierung (Vergleichsbasis) |
| `Examples/` | Anwendungsbeispiele, darunter ein Datensatz eines Einfeldträgers |
| `Plotting/` | Visualisierungsskripte |
| `Papers/` | Zugehörige Konferenz- und Zeitschriftenbeiträge |
| `methodology.pdf` | Visuelle Dokumentation des bayesschen Frameworks |

### Abhängigkeiten

```
numpy · scipy · tqdm · pyswarms
```
Python 3.13: Installation mit `pip install -r requirements.txt`

### Autorinnen und Autoren

Chiara Nardin · Stefano Zorzi · Federica Zonzini · Marco Broccardo

:bulb: Geben Sie dem Repository auf [GitHub](https://github.com/CNardin/Bay-Fi) einen Stern, um über Neuigkeiten informiert zu bleiben!
