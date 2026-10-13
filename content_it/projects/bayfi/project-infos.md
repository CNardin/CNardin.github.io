---
title: Informazioni e aggiornamenti
description: Informazioni dettagliate sul progetto Bay-Fi, con obiettivi, metodologia e attività di ricerca in corso.
date: 2025-10-27
weight: 2

toc: true
build:
  list: local
  render: always
---

## Abstract

Il monitoraggio strutturale (SHM) e l'analisi modale operativa si basano sull'identificazione accurata delle frequenze modali a partire dai segnali di vibrazione. In molti casi pratici, però, acquisire segnali ad alta frequenza è limitato dall'hardware, dal consumo energetico o dalla banda di trasmissione dei dati: il **campionamento Sub-Nyquist** diventa quindi una sfida centrale.

**Bay-Fi** (Bayesian Frequency Identification) affronta questa sfida con un nuovo metodo generale che consente l'**identificazione diretta della frequenza modale principale** senza richiedere:
- la ricostruzione del segnale
- alcuna taratura preliminare degli iperparametri

L'approccio usa un **framework bayesiano** per ottimizzare un algoritmo di curve fitting applicato a segnali di vibrazione fortemente sottocampionati e acquisiti in modo casuale. In questo modo si ottengono stime di frequenza robuste anche quando i metodi convenzionali fallirebbero per aliasing o dati insufficienti.

## Metodologia

L'idea centrale di Bay-Fi è riformulare l'identificazione della frequenza come un **problema di ottimizzazione bayesiana**. Invece di ricostruire l'intero segnale da misure sparse, il metodo stima direttamente la frequenza dominante adattando un modello parametrico ai campioni disponibili in un contesto probabilistico.

Caratteristiche principali del metodo:
- **Senza parametri da tarare**: non richiede conoscenze a priori né regolazioni manuali
- **Robusto al sottocampionamento**: funziona con segnali campionati ben al di sotto della frequenza di Nyquist
- **Compatibile con il campionamento casuale**: gestisce campioni non uniformi e acquisiti casualmente
- **Scalabile**: applicabile a misure a singolo canale e multicanale

## Podcast generato con l'IA

Ti sei mai chiesto come suonerebbe Bay-Fi spiegato da due conduttori entusiasti davanti a un caffè? Ecco la risposta. [Jari Vepsäläinen](https://research.aalto.fi/en/persons/jari-veps%C3%A4l%C3%A4inen/) (Aalto University, Finlandia) ha dato l'articolo in pasto a un'IA e ne è uscito un episodio di podcast sorprendentemente coinvolgente, con tanto di inferenza bayesiana e campionamento Sub-Nyquist. Buon ascolto! (Il podcast è in inglese.)

<iframe src="https://drive.google.com/file/d/1lN-NvHyULYmEGEZbyHjiGe6cebQHBFlp/preview" width="100%" height="80" allow="autoplay" style="border:none; border-radius:8px;"></iframe>

## Aggiornamenti

| Data | Aggiornamento |
| :--- | :----- |
| ott 2025 | Avvio del progetto, primo sviluppo del framework bayesiano |
