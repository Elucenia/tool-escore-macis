<!-- ELUCENIA technical documentation · escore-macis · zh · no clinical/professional/rights approval -->

# MACIS（甲状腺乳头状癌）

[条件、来源与许可](https://elucenia.org/zh/tools/escore-macis)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 诊断时年龄

`idade`

年 · 范围: 5–100

### 肿瘤最大直径

`tamanho`

cm · 范围: 0.1–20

### 是否切除不完全？

`incompleta`

- `0` — 否
- `1` — 是

### 是否有局部侵犯（甲状腺外）？

`invasao`

- `0` — 否
- `1` — 是

### 是否有远处转移？

`metastase`

- `0` — 否
- `1` — 是

## 方法版本

MACIS/Hay 1993：年龄/大小/切除/浸润/转移；至39岁为3.1，年龄≥40则0.08×年龄

## 已记录的公式

MACIS = 3.1 (若年龄 ≤ 39 岁) 或 0.08 × 年龄 (若年龄 ≥ 40 岁) + 0.3 × 肿瘤大小 (cm) + 1 (切除不完整) + 1 (局部浸润) + 3 (远处转移).

## 限制与适用人群

根据初次手术后可获得的数据评估甲状腺乳头状癌预后，包括切除完整性及以cm计的肿瘤大小。不应自动推广到其他组织学类型，或缺少切除信息的术前使用。校准属于所研究的历史队列。

## 参考文献

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
