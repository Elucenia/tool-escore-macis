<!-- ELUCENIA technical documentation · escore-macis · ja · no clinical/professional/rights approval -->

# MACIS（甲状腺乳頭癌）

[条件・出典・許諾](https://elucenia.org/ja/tools/escore-macis)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 診断時年齢

`idade`

年 · 範囲: 5–100

### 腫瘍最大径

`tamanho`

cm · 範囲: 0.1–20

### 不完全切除ですか？

`incompleta`

- `0` — いいえ
- `1` — はい

### 局所浸潤（甲状腺外）がありますか？

`invasao`

- `0` — いいえ
- `1` — はい

### 遠隔転移がありますか？

`metastase`

- `0` — いいえ
- `1` — はい

## 方法の版

MACIS/Hay 1993：年齢/径/切除/浸潤/転移；39歳まで3.1、40歳以上0.08×年齢

## 記載された計算式

MACIS = 3.1 (年齢が ≤ 39 歳) または 0.08 × 年齢 (年齢が ≥ 40 歳) + 0.3 × 腫瘍径 (cm) + 1 (不完全切除) + 1 (局所浸潤) + 3 (遠隔転移).

## 限界・対象集団

切除の完全性とcm単位の大きさを含む、初回手術後に得られるデータから甲状腺乳頭がんの予後を評価します。他の組織型や、切除の情報がない術前の使用へ自動的に外挿しないでください。較正は研究された歴史的コホートに属します。

## 参考文献

- [Hay ID et al. Predicting outcome in papillary thyroid carcinoma: development of a reliable prognostic scoring system in a cohort of 1779 patients surgically treated at one institution during 1940 through 1989. Surgery, 1993.](https://pubmed.ncbi.nlm.nih.gov/8256208/)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 記録された結果

以下の情報は、合成例に対する手法の出力を保持したものです。独立した臨床的検証を示すものではありません。

### 1

MACIS < 6：20年のがん特異的生存率は99%

| 結果の詳細 | |
| --- | --- |
| 年齢要素 | 3.10 |
| 大きさの要素 (0,3 × cm) | 0.60 |


### 2

MACIS 6 から 6,99：20年のがん特異的生存率は89%

| 結果の詳細 | |
| --- | --- |
| 年齢要素 | 4.40 |
| 大きさの要素 (0,3 × cm) | 1.50 |


### 3

MACIS 7 から 7,99：20年のがん特異的生存率は56%

| 結果の詳細 | |
| --- | --- |
| 年齢要素 | 4.80 |
| 大きさの要素 (0,3 × cm) | 1.20 |


### 4

MACIS ≥ 8：20年のがん特異的生存率は24%

| 結果の詳細 | |
| --- | --- |
| 年齢要素 | 5.60 |
| 大きさの要素 (0,3 × cm) | 1.50 |

