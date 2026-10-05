<!-- ELUCENIA technical documentation · escore-macis · es · no clinical/professional/rights approval -->

# MACIS (carcinoma papilar de tiroides)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/escore-macis)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Edad al diagnóstico

`idade`

años · intervalo: 5–100

### Diámetro mayor del tumor

`tamanho`

cm · intervalo: 0,1–20

### ¿Resección incompleta?

`incompleta`

- `0` — No
- `1` — Sí

### ¿Invasión local (extratiroidea)?

`invasao`

- `0` — No
- `1` — Sí

### ¿Metástasis a distancia?

`metastase`

- `0` — No
- `1` — Sí

## Edición del método

MACIS/Hay 1993: edad/tamaño/resección/invasión/metástasis; 3,1 hasta 39 años frente a 0,08×edad ≥40

## Fórmula documentada

MACIS = 3,1 (si edad ≤ 39 años) o 0,08 × edad (si edad ≥ 40 años) + 0,3 × tamaño tumoral (cm) + 1 (resección incompleta) + 1 (invasión local) + 3 (metástasis a distancia).

## Límites y población

Pronóstico del carcinoma papilar de tiroides a partir de datos disponibles después de la operación primaria, incluidas la integridad de la resección y el tamaño en cm. No extrapole automáticamente a otra histología ni al uso preoperatorio sin información sobre la resección. La calibración pertenece a las cohortes históricas estudiadas.

## Referencias

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
