<!-- ELUCENIA technical documentation · escore-macis · de · no clinical/professional/rights approval -->

# MACIS (papilläres Schilddrüsenkarzinom)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/escore-macis)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Alter bei Diagnose

`idade`

Jahre · Bereich: 5–100

### Größter Tumordurchmesser

`tamanho`

cm · Bereich: 0,1–20

### Unvollständige Resektion?

`incompleta`

- `0` — Nein
- `1` — Ja

### Lokale Invasion (extrathyreoidal)?

`invasao`

- `0` — Nein
- `1` — Ja

### Fernmetastase?

`metastase`

- `0` — Nein
- `1` — Ja

## Fassung der Methode

MACIS/Hay 1993: Alter/Größe/Resektion/Invasion/Metastasen; 3,1 bis 39 Jahre gegenüber 0,08×Alter ≥40

## Dokumentierte Formel

MACIS = 3,1 (bei Alter ≤ 39 Jahre) oder 0,08 × Alter (bei Alter ≥ 40 Jahre) + 0,3 × Tumorgröße (cm) + 1 (unvollständige Resektion) + 1 (lokale Invasion) + 3 (Fernmetastasen).

## Grenzen und Population

Prognose des papillären Schilddrüsenkarzinoms anhand von nach der primären Operation verfügbaren Daten einschließlich Resektionsvollständigkeit und Größe in cm. Nicht automatisch auf andere Histologien oder präoperative Anwendung ohne Resektionsinformation übertragen. Die Kalibrierung gehört zu den untersuchten historischen Kohorten.

## Referenzen

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Dokumentierte Ergebnisse

Die folgenden Angaben bewahren die Ausgaben der Methode für synthetische Beispiele. Sie stellen keine unabhängige klinische Validierung dar.

### 1

MACIS < 6: 20-Jahres-krebsspezifisches Überleben von 99%

| Ergebnisdetails | |
| --- | --- |
| Alterskomponente | 3,10 |
| Größenkomponente (0,3 × cm) | 0,60 |


### 2

MACIS 6 bis 6,99: 20-Jahres-krebsspezifisches Überleben von 89%

| Ergebnisdetails | |
| --- | --- |
| Alterskomponente | 4,40 |
| Größenkomponente (0,3 × cm) | 1,50 |


### 3

MACIS 7 bis 7,99: 20-Jahres-krebsspezifisches Überleben von 56%

| Ergebnisdetails | |
| --- | --- |
| Alterskomponente | 4,80 |
| Größenkomponente (0,3 × cm) | 1,20 |


### 4

MACIS ≥ 8: 20-Jahres-krebsspezifisches Überleben von 24%

| Ergebnisdetails | |
| --- | --- |
| Alterskomponente | 5,60 |
| Größenkomponente (0,3 × cm) | 1,50 |

