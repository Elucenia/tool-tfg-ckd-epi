<!-- ELUCENIA technical documentation · tfg-ckd-epi · ja · no clinical/professional/rights approval -->

# 糸球体濾過量（CKD-EPI 2021）

[条件・出典・許諾](https://elucenia.org/ja/tools/tfg-ckd-epi)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 血清クレアチニン

`cr`

mg/dL · 範囲: 0.2–20

### 年齢

`idade`

年 · 範囲: 18–110

### 性別

`sexo`

- `F` — 女性
- `M` — 男性

## 方法の版

CKD-EPIクレアチニン2021/Inker：人種なし142, min/max,κ0.7/0.9,α−0.241/−0.302、シスタチンなし

## 記載された計算式

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1.200 × 0.9938年齢 × 1.012 (女性).

κ = 0.7 (女性) または 0.9 (男性); α = −0.241 (女性) または −0.302 (男性). 結果単位 mL/min/1.73 m².

## 限界・対象集団

18歳以上の成人を対象とする、クレアチニンのみを用いたCKD-EPI2021式です。IDMSで標準化された血清クレアチニン値が必要です。結果はmL/min/1.73m²で表す推算値であり、濾過量を直接測定した値ではありません。腎機能が不安定な場合、妊娠、重篤な疾患、がん、非典型的な筋肉量や体格では、信頼性が低下する可能性があります。判断の閾値に近い場合、評価にはクレアチニンとシスタチンCを併用した推算、または確認のための測定が必要になることがあります。G区分だけでは慢性腎臓病を確認できません。体表面積で補正された結果を、薬剤用量に用いる絶対クリアランスとして自動的に扱わないでください。添付文書、対象集団、必要な方法を確認してください。

## 参考文献

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

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
