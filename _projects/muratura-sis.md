---
title: "Masonry"
excerpt: "Valutazione di rischio sismico per un edificio esistente in muratura
."
header:
  teaser: /_projects/images/classificazioneRS.jpg
sidebar:
  nav: "projects"
toc: true
toc_label: "Contenuti"
toc_icon: "columns"
toc_sticky: true
---
<!-- header:
  image: /_projects/images/classificazioneRS.jpg
  teaser: /_projects/images/classificazioneRS.jpg
 -->

![](/projects/images/classificazioneRS.jpg){:height="75px" align="right" }
# Valutazione di rischio sismico per un edificio esistente in muratura

## Obiettivi

:black_medium_small_square: Valutazione dell'indice di sicurezza IS-V di un edificio esistente in muratura

:black_medium_small_square: Progettazione degli interventi consolidamento necessari per l'accesso alle agevolazioni fiscali previste dal [Sisma Bonus](https://www.agenziaentrate.gov.it/portale/documents/20143/233439/Sisma+bonus+le+detrazioni+per+gli+interventi+antisismici_Guida_Sisma_Bonus.pdf/ee5ec719-05ae-0584-897e-f60d34060498 "Link Agenzia Entrate").

## Caso Applicativo
Edificio residenziale in muratura risalente al secondo dopo guerra, sito nel centro storico del capoluogo trentino.
![Google Earth](/projects/images/locate.gif)

## Indagini Conoscitive Preliminari
Per le strutture esistenti, le indagini e gli studi preliminari volti alla determinazione del *livello di conoscenza*, come indicato al [§C8][2].1, risultano essere di fondamentale importanza.  
Il livello di conoscenza *LC* è in generale funzione della geometria, dei dettagli costruttivi e delle proprietà dei materiali. Per la struttura in esame, in base ai rilievi e alle indagini su dettagli costruttivi e proprietà dei materiali, si è assunto un livello di conoscenza *LC1*, a cui si associa un fattore di confidenza pari a *FC=1.35*. Tale fattore interverrà poi nella definizione dei valori caratteristici di progetto dei materiali della struttura.

<!-- ![](/projects/images/muratura-sis6.png)
 -->
## Modellazione 
Da piante e prospetti dell'edificio, si costruisce il modello ad elementi finiti FEM tramite software di calcolo SAP2000. 
Tale modello servirà sia come supporto per la determinazione ed il calcolo degli interventi di consolidamento necessari, sia come strumento di valutazione del livello di sicurezza della struttura *ante* e *post operam*.

Data la geometria e la complessità del caso, si è pertanto deciso di procedere mediante schematizzazione a telaio equivalente, secondo quanto riportato in [Dolce][3]. 
![Schema Telaio Equivalente](/projects/images/muratura-sis7.png)

In particolare, con questa metodologia ogni parete risulta essere costituita da tre macro-elementi:

* maschi murari, ovvero gli elementi verticali deformabili posti tra due aperture adiacenti allo stesso livello;
* fasce di piano (o travi di accoppiamento), ovvero gli elementi orizzontali deformabili posti tra due aperture adiacenti a livelli diversi;
* nodi rigidi, ovvero gli elementi d’intersezione tra il maschio murario e la fascia di piano.

Per maggiori dettagli riguardanti le tecniche e scelte impiegate nella modellazione si rimanda alla relativa relazione di calcolo.

Si è prestata inoltre particolare attenzione alla modellazione dei solai in quanto, l'usuale ipotesi nelle nuove costruzioni di orizzontamento infinitamente rigido, deve essere debitamente indagata nelle strutture esistenti, a causa dei limitati spessori e rigidezze dei solai. 
Infatti, , come in questo caso, con solai lignei a semplice o doppia orditura, va considerata nel modello la loro [deformabilità nel piano][5]. Sono state pertanto assegnate due rigidezze diverse nelle direzioni principale e secondaria del solaio, proporzionali ai rispettivi moduli di elasticità delle sezioni delle travi lignee del solaio e dell’assito.


Infine, relativamente alla validazione del modello, si è operato un confronto fra il taglio alla base risultante da un'analisi statica lineare con quello risultante da un'analisi dinamica lineare. 
Si riportano di seguito anche i modi di vibrare fondamentali della struttura in esame.

![](/_projects/images/muratura-sis0.png)

## Progettazione degli interventi
Avendo individuato come problematica principale su cui intervenire i solai esistenti con singolo assito, si è valutato un intervento di rifacimento della stratigrafia esistente col fine di assicurare un massetto > 5 cm per garantire una ridistribuzione delle azioni nel piano e un efficace ammorsamento delle travi alla struttura portante in muratura.

![](/_projects/images/muratura-sis2.png){:height="165px"}
![](/_projects/images/muratura-sis4.png){:height="165px" align="right"}

## Classificazione rischio sismico

Valutare l'indice IS-V allo stato di fatto significa condurre analisi push-over 
1. non linearità → cerniere plastiche → definite tramite P-M2-M3 per tener conto del taglio e della sua influenza 
2. profili di carico

Alcuni risultati delle pushover
![](/_projects/images/muratura-sis1.png)
Si valutano quindi PAM e IS-V

## Conclusioni
Passaggio di 2 classi


![](/_projects/images/muratura-sis3.png)


## Riferimenti utili
### Normativi
* D.M. 28 febbraio 2017 e D.M. 7 marzo 2017 (linee guida per la classificazione del rischio sismico delle costruzioni) - decreti pubblicati sul sito del 
[Ministero delle Infrastrutture e dei Trasporti](https://www.mit.gov.it/ "DM 28/02/2017 - DM 07/03/2017")

* D.M. n. 24 del 9/1/2020 contenente le linee guida per la classificazione del rischio sismico delle costruzioni nonché le modalità per l'attestazione, da parte di professionisti abilitati, dell'efficacia degli interventi effettuati.
[D.M.24 - 09/01/2020](https://www.mit.gov.it/normativa/decreto-ministeriale-numero-24-del-09012020 "Decreto Sisma Bonus")

* [Norme Tecniche per le Costruzioni 17 Gennaio 2018](https://www.gazzettaufficiale.it/eli/gu/2018/02/20/42/so/8/sg/pdf), Gazzetta Ufficiale del 20 Febbraio 2018, Ministero delle Infrastrutture e dei Trasporti.

* [Circolare 21 Gennaio 2019](https://www.gazzettaufficiale.it/eli/id/2019/02/11/19A00855/sg), n.7 C.S.LL.PP. Istruzioni per l’applicazione dell’aggiornamento delle “Norme tecniche per le costruzioni” di cui al decreto ministeriale 17 Gennaio 2018, Supplemento ordinario alla Gazzetta Ufficiale, n.35 dell’11 Febbraio 2019, Ministero delle Infrastrutture e dei Trasporti.

* Linee guida. [Classificazione della vulnerabilità degli edifici ai fini della valutazione del rischio sismico](http://www.difesa.it/SMD_/CASD/IM/CeMiSS/Pubblicazioni/ricerche/Pagine/Metta_AO_SGD_04.aspx) - Ministero delle Infrastrutture e dei Trasporti DM 17/10/2013.


### Bibliografici
* Dolce, M., (1989). Schematizzazione e modellazione per azioni nel piano delle pareti, [Corso sul consolidamento degli edifici in muratura in zona sismica.](https://www.leca.it/wp-content/uploads/2020/07/Edifici-in-muratura-ordinaria-e-armata-prof-Magenes.pdf) Ordine degli Ingegneri, Potenza. 

* Magenes, G., Calvi, G. M., (1997). [In-plane seismic response of brick masonry walls](https://onlinelibrary.wiley.com/doi/abs/10.1002/%28SICI%291096-9845%28199711%2926%3A11%3C1091%3A%3AAID-EQE693%3E3.0.CO%3B2-6). Earthquake Engineering and Structural Dynamics, 26, 1091-1112.

* Magenes, G., Bolognini, D., Braggio, C. (2000). [Metodi semplificati per l'analisi sismica non lineare di edifici in muratura.](https://emidius.mi.ingv.it/GNDT2/Pubblicazioni/Magenes_copertina_con_intestazione.htm) CNR-Gruppo Nazionale per la Difesa dai Terremoti. Rome. 

* Giongo, I., Piazza, M., Tomasi, R. (2010) [Pushover analysis of traditional masonry buildings: influence of refurbished timber-floors stiffness](http://www.rewis.it/download/rigidezza_solai.pdf). REWIS.

 
[2]: <https://www.gazzettaufficiale.it/eli/id/2019/02/11/19A00855/sg> "[Circolare 21 Gennaio 2019](https://www.gazzettaufficiale.it/eli/id/2019/02/11/19A00855/sg), n.7 C.S.LL.PP. Istruzioni per l’applicazione dell’aggiornamento delle “Norme tecniche per le costruzioni” di cui al decreto ministeriale 17 Gennaio 2018, Supplemento ordinario alla Gazzetta Ufficiale, n.35 dell’11 Febbraio 2019, Ministero delle Infrastrutture e dei Trasporti."
[3]: "Dolce, M., (1989). Schematizzazione e modellazione per azioni nel piano delle pareti, [Corso sul consolidamento degli edifici in muratura in zona sismica.](https://www.leca.it/wp-content/uploads/2020/07/Edifici-in-muratura-ordinaria-e-armata-prof-Magenes.pdf) Ordine degli Ingegneri, Potenza." 
[4]: "Magenes, G., Bolognini, D., Braggio, C. (2000). [Metodi semplificati per l'analisi sismica non lineare di edifici in muratura.](https://emidius.mi.ingv.it/GNDT2/Pubblicazioni/Magenes_copertina_con_intestazione.htm) CNR-Gruppo Nazionale per la Difesa dai Terremoti. Rome." 
[5]: "Giongo, I., Piazza, M., Tomasi, R. (2010) [Pushover analysis of traditional masonry buildings: influence of refurbished timber-floors stiffness](http://www.rewis.it/download/rigidezza_solai.pdf). REWIS." 
