---
linkTitle: Bay-Fi
title: Bay-Fi
date: 2025-10-27
type: docs
summary: "Bay-Fi (Bayesian Frequency Identification) è un nuovo metodo per identificare direttamente le frequenze modali da segnali di vibrazione fortemente sottocampionati, senza ricostruzione del segnale né taratura preliminare."
build:
  list: always
  render: always

tags:
  - Bay-Fi
  - System Identification
  - Sub-Nyquist

toc: true
weight: 2
sidebar:
  open: true
---

Questa è la pagina del progetto **Bay-Fi**, acronimo di **Bayesian Frequency Identification**. Lo studio introduce un nuovo metodo generale che permette di identificare direttamente la frequenza modale principale senza ricostruire il segnale e senza alcuna taratura preliminare. L'approccio usa un framework bayesiano per ottimizzare un algoritmo di curve fitting applicato a segnali di vibrazione fortemente sottocampionati e acquisiti in modo casuale.

Il metodo è particolarmente adatto agli scenari di **campionamento Sub-Nyquist**, in cui le tecniche convenzionali di elaborazione del segnale falliscono a causa dell'aliasing e di frequenze di campionamento insufficienti. Grazie all'inferenza bayesiana, Bay-Fi fornisce stime di frequenza robuste e accurate anche da misure fortemente compresse.

Qui trovi maggiori informazioni sul progetto e sulle attività di ricerca in corso:

- {{< cards >}}
  {{< card url="/it/projects/bayfi/project-infos/" title="Informazioni e aggiornamenti" icon="document-duplicate" >}}
  {{< /cards >}}
- {{< cards >}}
  {{< card url="/it/projects/bayfi/bayfi-references/" title="Pubblicazioni e presentazioni" icon="document-duplicate" >}}
  {{< /cards >}}
- {{< cards >}}
  {{< card url="/it/projects/bayfi/repository/" title="Codice" icon="code-bracket" >}}
  {{< /cards >}}
