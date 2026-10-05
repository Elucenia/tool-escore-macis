<!-- ELUCENIA technical documentation · escore-macis · fr · no clinical/professional/rights approval -->

# MACIS (carcinome papillaire thyroïdien)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/escore-macis)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Âge au diagnostic

`idade`

ans · intervalle: 5–100

### Plus grand diamètre tumoral

`tamanho`

cm · intervalle: 0,1–20

### Résection incomplète ?

`incompleta`

- `0` — Non
- `1` — Oui

### Invasion locale (extrathyroïdienne) ?

`invasao`

- `0` — Non
- `1` — Oui

### Métastase à distance ?

`metastase`

- `0` — Non
- `1` — Oui

## Édition de la méthode

MACIS/Hay 1993 : âge/taille/résection/invasion/métastases ; 3,1 jusqu’à 39 ans contre 0,08×âge ≥40

## Formule documentée

MACIS = 3,1 (si âge ≤ 39 ans) ou 0,08 × âge (si âge ≥ 40 ans) + 0,3 × taille tumorale (cm) + 1 (résection incomplète) + 1 (invasion locale) + 3 (métastases à distance).

## Limites et population

Pronostic du carcinome papillaire de la thyroïde à partir des données disponibles après l’opération primaire, dont la complétude de la résection et la taille en cm. Ne pas extrapoler automatiquement à une autre histologie ou à un usage préopératoire sans information sur la résection. Le calibrage appartient aux cohortes historiques étudiées.

## Références

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
