<!-- ELUCENIA technical documentation · escore-macis · it · no clinical/professional/rights approval -->

# MACIS (carcinoma papillare della tiroide)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/escore-macis)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Età alla diagnosi

`idade`

anni · intervallo: 5–100

### Diametro maggiore del tumore

`tamanho`

cm · intervallo: 0,1–20

### Resezione incompleta?

`incompleta`

- `0` — No
- `1` — Sì

### Invasione locale (extratiroidea)?

`invasao`

- `0` — No
- `1` — Sì

### Metastasi a distanza?

`metastase`

- `0` — No
- `1` — Sì

## Edizione del metodo

MACIS/Hay 1993: età/dimensioni/resezione/invasione/metastasi; 3,1 fino a 39 anni versus 0,08×età ≥40

## Formula documentata

MACIS = 3,1 (se età ≤ 39 anni) o 0,08 × età (se età ≥ 40 anni) + 0,3 × dimensione tumorale (cm) + 1 (resezione incompleta) + 1 (invasione locale) + 3 (metastasi a distanza).

## Limiti e popolazione

Prognosi del carcinoma papillare della tiroide dai dati disponibili dopo l’intervento primario, inclusi la completezza della resezione e le dimensioni in cm. Non estrapolare automaticamente ad altre istologie o all’uso preoperatorio senza informazioni sulla resezione. La calibrazione appartiene alle coorti storiche studiate.

## Riferimenti

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
