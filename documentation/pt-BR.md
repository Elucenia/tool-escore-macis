<!-- ELUCENIA technical documentation · escore-macis · pt-BR · no clinical/professional/rights approval -->

# MACIS (carcinoma papilífero de tireoide)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/escore-macis)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Idade no diagnóstico

`idade`

anos · intervalo: 5–100

### Maior diâmetro do tumor

`tamanho`

cm · intervalo: 0,1–20

### Ressecção incompleta?

`incompleta`

- `0` — Não
- `1` — Sim

### Invasão local (extratireoidiana)?

`invasao`

- `0` — Não
- `1` — Sim

### Metástase a distância?

`metastase`

- `0` — Não
- `1` — Sim

## Edição do método

MACIS/Hay 1993:idade/tamanho/ressecção/invasão/metástase; 3,1 até 39 anos vs 0,08 idade≥40

## Fórmula documentada

MACIS = 3,1 (se idade ≤ 39 anos) ou 0,08 × idade (se ≥ 40 anos) + 0,3 × tamanho do tumor (cm) + 1 (ressecção incompleta) + 1 (invasão local) + 3 (metástase a distância).

## Limites e população

Prognóstico de carcinoma papilífero da tireoide a partir de dados disponíveis após a operação primária, incluindo completude da ressecção e tamanho em cm. Não extrapolar automaticamente para outra histologia ou uso pré-operatório sem informação de ressecção. A calibração pertence às coortes históricas estudadas.

## Referências

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

MACIS < 6: sobrevida câncer-específica em 20 anos de 99%

| Detalhes do resultado | |
| --- | --- |
| Componente da idade | 3,10 |
| Componente do tamanho (0,3 × cm) | 0,60 |


### 2

MACIS 6 a 6,99: sobrevida câncer-específica em 20 anos de 89%

| Detalhes do resultado | |
| --- | --- |
| Componente da idade | 4,40 |
| Componente do tamanho (0,3 × cm) | 1,50 |


### 3

MACIS 7 a 7,99: sobrevida câncer-específica em 20 anos de 56%

| Detalhes do resultado | |
| --- | --- |
| Componente da idade | 4,80 |
| Componente do tamanho (0,3 × cm) | 1,20 |


### 4

MACIS ≥ 8: sobrevida câncer-específica em 20 anos de 24%

| Detalhes do resultado | |
| --- | --- |
| Componente da idade | 5,60 |
| Componente do tamanho (0,3 × cm) | 1,50 |

