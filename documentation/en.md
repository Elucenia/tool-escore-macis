<!-- ELUCENIA technical documentation · escore-macis · en · no clinical/professional/rights approval -->

# MACIS (papillary thyroid carcinoma)

[conditions, sources and permissions](https://elucenia.org/en/tools/escore-macis)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Age at diagnosis

`idade`

years · range: 5–100

### Largest tumor diameter

`tamanho`

cm · range: 0.1–20

### Incomplete resection?

`incompleta`

- `0` — No
- `1` — Yes

### Local invasion (extrathyroidal)?

`invasao`

- `0` — No
- `1` — Yes

### Distant metastasis?

`metastase`

- `0` — No
- `1` — Yes

## Method edition

MACIS/Hay 1993: age/size/resection/invasion/metastasis; 3.1 up to age 39 versus 0.08×age ≥40

## Documented formula

MACIS = 3.1 (if age ≤ 39 years) or 0.08 × age (if age ≥ 40 years) + 0.3 × tumor size (cm) + 1 (incomplete resection) + 1 (local invasion) + 3 (distant metastasis).

## Limits and population

Prognosis of papillary thyroid carcinoma from data available after the primary operation, including completeness of resection and size in cm. Do not automatically extrapolate to another histology or preoperative use without resection information. Calibration belongs to the historical cohorts studied.

## References

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
