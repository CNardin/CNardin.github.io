# TODO – cose da fornire, correggere e controllare nel sito

Riferimento: CV `C:\SVN\myPersonal\concorsi\2026-centralesupelec\cv\CV-cnardin.pdf`
Ultimo aggiornamento: 2026-10-13

## Subito
- [ ] **Riavviare `hugo server`** (Ctrl+C, poi `hugo server`): il server aperto non ha caricato la configurazione multilingua.
- [ ] **Nessuna modifica è ancora committata.** Fare commit e push quando le verifiche sono concluse.

## PDF mancanti o da sostituire

### Conferenze (`content/publication/conferences/`)
- [ ] **C11 – SEDIF 2020** (`2020-SEDIF-spif`): manca il PDF (paper o abstract).
      Marinković et al., Apprimus Verlag, pp. 159–172, ISBN 978-3-86359-729-0.
      Da verificare: elenco completo dei 19 autori (ora c'è "et al."), abstract (scritto a mano), data (ora 2020-03-04).
- [ ] **C7 – WCEE 2024 Alto Garda** (`2024-WCEE-maers`): ci sono solo le slide (ETH Research Collection);
      manca il paper o l'abstract pubblicato.
- [ ] **C8 – WCEE 2024 serbatoi** (`2024-WCEE-tank`): c'è la versione autore; mancano un DOI o un link editore
      e la data esatta (ora 2024-07-01).
- [ ] **C6, C9, C10 – ASME PVP 2024/2021** (`2024-PVP-bfj`, `2021-PVP-spif`, `2021-PVP-mcs`): ci sono solo le versioni autore.
      Verificare che il copyright ASME ne consenta la pubblicazione, oppure fornire le versioni consentite.
- [ ] Date indicative da confermare: C1/C2 REC 2026 (2026-08-01).

### Articoli (`content/publication/articles/`)
- [ ] **J9 – SPIF dataset** (`2021-DATA-spif`): mancano il PDF, il DOI o il link al repository e la data reale
      (ora 2021-01-01 è un segnaposto).
- [ ] **RESS 2025**: `static/papers/RESS_2025_Nardin.pdf` è danneggiato (errori xref); serve una copia integra.

## Foto e profili coautori (`assets/media/authors/`, `data/authors/`)
- [ ] Foto mancanti: Valerio Vezzari, Alessandra Marino, Mariano Ciucci, Tugberk Guner, Silvano Erlicher,
      Alexandre Monteil, Carlo Costa, Styfen Schär, Stefano Parolai, Daniele Zonta, Federico Ugolini, Stefano Zorzi.
- [ ] Link alle pagine web mancanti o deboli: Vezzari (nessun link); Marino, Ciucci, Guner, Erlicher, Monteil, Schär,
      Parolai, Zonta (solo ORCID); Costa (pagina di un sito di conferenze).
- [ ] Confermare l'identità e l'affiliazione di Erlicher e Monteil (abbinati su ORCID solo per nome).
- [ ] Guner: su ORCID il nome è "Tuğberk Güner"; sul sito è "Guner", come nel paper. Decidere quale tenere.
- [ ] Butenweg: la pagina FH Aachen blocca i bot (403), quindi il link non è stato verificato.

## Contenuti mancanti
- [ ] **Preprint P1 e P2**: pagine non ancora create. I link pubblici sono noti (P1 arXiv:2606.12448, P2 SSRN 7270402):
      basta una conferma per crearle. Opzionale: un'immagine preferita.

## Segnaposto ed errori nelle pagine (da correggere in EN, IT e DE)
- [ ] **REACTIS** (`projects/reactis/_index.md`): il summary inglese è ancora quello del template
      ("An open-source tool for automated data analysis"). IT e DE hanno già un summary corretto.
- [ ] **MAERS – pubblicazioni** (`projects/maers/maers-references.md`):
      - "J1. ..." è un segnaposto e punta all'articolo RESS;
      - C2 (WCEE 2024) non ha link, ma ora esiste la pagina `conferences/2024-WCEE-maers`;
      - il poster P1 punta alla pagina ANIDIS.
- [ ] **SPIF** (`projects/spif/index.md`): la tabella "Related publications" contiene il segnaposto "j1. AA".
- [ ] **Esperienza**: il pulsante "View project" punta a `/reactis`, che non esiste (dovrebbe essere `/projects/reactis/`).
- [x] **REACTIS – riferimenti**: stato dei talk aggiornato (CSM 2026, WiDS 2026 e REC 2026 presentati).
- [ ] **REACTIS – webinar IASSAR TC R3 (29 ott 2026)**: dopo il 29 ottobre segnare T7 come presentato (EN/IT/DE); eventuale link a slide/registrazione.
- [ ] **MAERS – 50° Santa Lucia (11 dic 2026)**: quando la locandina è definitiva, sostituire "release soon" con il link al PDF (`projects/maers/news.md` e news `2026-SantaLucia50-maers`, EN/IT/DE). Ora `locandina_tecnica_v4.pdf` è in `content/projects/maers/` non linkato.
- [ ] **REACTIS e repository**: il "Tip: Remember to appreciate the little things in life" è un testo demo. Tenerlo?

## Sito multilingua (EN / IT / DE)
Struttura: le traduzioni stanno in `content_it/` e `content_de/` con gli stessi percorsi di `content/`;
le pagine non tradotte mostrano il testo inglese (fallback configurato in `config/_default/module.yaml`).
Bio/Esperienza tradotte in `data/authors_i18n/<lingua>/chiara-nardin.yaml`; stringhe del tema in `i18n/it.yaml`.
- [ ] Rileggere le traduzioni tedesche (Bio, Esperienza, progetti, news, contatti). Il tedesco usa la "ß" standard
      (es. "Fließend"); decidere se passare alla grafia svizzera ("ss").
- [ ] Rileggere le traduzioni italiane.
- [ ] Ogni pagina nuova o modificata in `content/` va aggiornata anche in `content_it/` e `content_de/`
      (altrimenti in IT/DE compare il testo inglese, o la vecchia traduzione).
- [ ] Pubblicazioni: per scelta restano in inglese in tutte le lingue.
- [ ] Footer "Ultima modifica": la data va aggiornata in tre punti, cioè `params.yaml` (EN) e `languages.yaml` (IT, DE).

## Decisioni richieste
- [ ] **J2 – CET 2025** (`conferences/2025-CET-tank`): nel CV è un articolo su rivista. Spostarlo in `articles/`?
- [ ] **EURODYN 2020** (`conferences/2020-EURODYN-spif`): è nel sito ma non nel CV. Tenerlo?
- [ ] **`articles/2025-a`**: è la pagina di esempio di Hugo Blox. Eliminarla?
- [x] **Sezioni demo `blog/`, `courses/`, `events/`, `slides/`**: escluse dalla pubblicazione con
      `build: render/list: never` (non compaiono in sito, sitemap e ricerca; i file restano).
      ⚠️ **Da NON tradurre mai**: niente file `.it.md`/`.de.md` per queste sezioni.
- [ ] **Preprint e news**: convertire gli autori in slug come per articoli e conferenze?
- [ ] **Google Search Console** (facoltativo): chiedere la rimozione degli URL demo già indicizzati
      (`/blog/`, `/courses/`, `/events/`, `/slides/`).
