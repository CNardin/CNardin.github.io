---
title: Projektinfos & Neuigkeiten
description: Ausführliche Informationen zum Projekt Bay-Fi, mit Zielen, Methodik und laufenden Forschungsarbeiten.
date: 2025-10-27
weight: 2

toc: true
build:
  list: local
  render: always
---

## Abstract

Bauwerksüberwachung (SHM) und operationelle Modalanalyse beruhen auf der genauen Identifikation modaler Frequenzen aus Schwingungssignalen. In vielen praktischen Fällen ist die Erfassung hochfrequenter Signale jedoch durch Hardware, Energieverbrauch oder Übertragungsbandbreite begrenzt, wodurch die **Sub-Nyquist-Abtastung** zu einer zentralen Herausforderung wird.

**Bay-Fi** (Bayesian Frequency Identification) begegnet dieser Herausforderung mit einer neuen, allgemeinen Methode, die die **direkte Identifikation der modalen Hauptfrequenz** ermöglicht, ohne:
- Signalrekonstruktion
- vorherige Abstimmung von Hyperparametern

Der Ansatz nutzt ein **bayessches Framework**, um einen Kurvenanpassungsalgorithmus zu optimieren, der auf stark unterabgetastete und zufällig erfasste Schwingungssignale angewendet wird. So entstehen robuste Frequenzschätzungen auch dort, wo herkömmliche Methoden wegen Aliasing oder zu weniger Daten scheitern würden.

## Methodik

Die Kernidee von Bay-Fi besteht darin, die Frequenzidentifikation als **bayessches Optimierungsproblem** zu formulieren. Statt das vollständige Signal aus spärlichen Messungen zu rekonstruieren, schätzt die Methode die dominante Frequenz direkt, indem sie ein parametrisches Modell in einem probabilistischen Rahmen an die verfügbaren Abtastwerte anpasst.

Wesentliche Merkmale der Methode:
- **Ohne Parameterabstimmung**: kein Vorwissen und keine manuelle Einstellung erforderlich
- **Robust gegenüber Unterabtastung**: funktioniert mit Signalen, die deutlich unterhalb der Nyquist-Rate abgetastet sind
- **Für zufällige Abtastung geeignet**: verarbeitet ungleichmäßige und zufällig erfasste Abtastwerte
- **Skalierbar**: anwendbar auf Ein- und Mehrkanalmessungen

## KI-generierter Podcast

Haben Sie sich je gefragt, wie Bay-Fi klingen würde, wenn zwei begeisterte Moderatoren es bei einem Kaffee erklären? Hier ist die Antwort. [Jari Vepsäläinen](https://research.aalto.fi/en/persons/jari-veps%C3%A4l%C3%A4inen/) (Aalto University, Finnland) hat das Paper einer KI gegeben, und heraus kam eine überraschend unterhaltsame Podcast-Folge, mit bayesscher Inferenz, Sub-Nyquist-Abtastung und allem Drum und Dran. Viel Spaß beim Zuhören! (Der Podcast ist auf Englisch.)

<iframe src="https://drive.google.com/file/d/1lN-NvHyULYmEGEZbyHjiGe6cebQHBFlp/preview" width="100%" height="80" allow="autoplay" style="border:none; border-radius:8px;"></iframe>

## Neuigkeiten

| Datum | Neuigkeit |
| :--- | :----- |
| Okt. 2025 | Projektstart, erste Entwicklung des bayesschen Frameworks |
