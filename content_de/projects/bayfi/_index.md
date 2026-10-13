---
linkTitle: Bay-Fi
title: Bay-Fi
date: 2025-10-27
type: docs
summary: "Bay-Fi (Bayesian Frequency Identification) ist eine neue Methode zur direkten Identifikation modaler Frequenzen aus stark unterabgetasteten Schwingungssignalen, ohne Signalrekonstruktion und ohne vorherige Abstimmung."
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

Dies ist die Projektseite von **Bay-Fi**, kurz für **Bayesian Frequency Identification**. Die Studie stellt eine neue, allgemeine Methode vor, mit der sich die modale Hauptfrequenz direkt identifizieren lässt, ohne das Signal zu rekonstruieren und ohne vorherige Abstimmung. Der Ansatz nutzt ein bayessches Framework, um einen Kurvenanpassungsalgorithmus zu optimieren, der auf stark unterabgetastete und zufällig erfasste Schwingungssignale angewendet wird.

Die Methode eignet sich besonders für **Sub-Nyquist-Abtastung**, bei der herkömmliche Signalverarbeitungsverfahren wegen Aliasing und unzureichender Abtastraten versagen. Dank bayesscher Inferenz liefert Bay-Fi robuste und genaue Frequenzschätzungen selbst aus stark komprimierten Messungen.

Hier finden Sie weitere Informationen zum Projekt und zu den laufenden Forschungsarbeiten:

- {{< cards >}}
  {{< card url="/de/projects/bayfi/project-infos/" title="Projektinfos & Neuigkeiten" icon="document-duplicate" >}}
  {{< /cards >}}
- {{< cards >}}
  {{< card url="/de/projects/bayfi/bayfi-references/" title="Publikationen und Vorträge" icon="document-duplicate" >}}
  {{< /cards >}}
- {{< cards >}}
  {{< card url="/de/projects/bayfi/repository/" title="Code-Repository" icon="code-bracket" >}}
  {{< /cards >}}
