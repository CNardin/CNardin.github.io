---
title: Codice
description: Accesso al repository del codice del progetto Bay-Fi, con i link al repository GitHub, al codice sorgente e alla documentazione.
date: 2025-10-27
weight: 4

toc: true
build:
  list: local
  render: always
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

## <i class="fa-brands fa-github"></i> Bay-Fi

Il codice sorgente di Bay-Fi è disponibile liberamente su GitHub con **licenza MIT**.

| | | | |
| :- | :- | :- | :- |
| [![GitHub](https://img.shields.io/badge/Source-GitHub-181717?logo=github)](https://github.com/CNardin/Bay-Fi) | ![License](https://img.shields.io/badge/License-MIT-blue) | ![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white) | ![Topics](https://img.shields.io/badge/SHM-Bayesian-green) |

> Bay-Fi è un framework bayesiano per estrarre le principali frequenze di vibrazione da segnali estremamente sparsi e sottocampionati, senza ricostruzione del segnale né taratura dei parametri. Raggiunge rapporti di compressione più elevati rispetto agli approcci tradizionali di compressed sensing.

### Struttura del repository

| Cartella | Descrizione |
| :----- | :---------- |
| `BayFi/` | Algoritmo principale: libreria `LIB.py` |
| `Classic-CS/` | Routine MATLAB di ottimizzazione convessa (riferimento per il confronto) |
| `Examples/` | Esempi applicativi, tra cui un dataset di trave semplicemente appoggiata |
| `Plotting/` | Script di visualizzazione |
| `Papers/` | Articoli a conferenze e su rivista correlati |
| `methodology.pdf` | Documentazione visiva del framework bayesiano |

### Dipendenze

```
numpy · scipy · tqdm · pyswarms
```
Python 3.13: installazione con `pip install -r requirements.txt`

### Autori

Chiara Nardin · Stefano Zorzi · Federica Zonzini · Marco Broccardo

:bulb: Metti una stella al repository su [GitHub](https://github.com/CNardin/Bay-Fi) per seguire gli aggiornamenti!
