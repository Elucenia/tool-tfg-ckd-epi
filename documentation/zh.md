<!-- ELUCENIA technical documentation · tfg-ckd-epi · zh · no clinical/professional/rights approval -->

# 肾小球滤过率（CKD-EPI 2021）

[条件、来源与许可](https://elucenia.org/zh/tools/tfg-ckd-epi)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 血清肌酐

`cr`

mg/dL · 范围: 0.2–20

### 年龄

`idade`

年 · 范围: 18–110

### 性别

`sexo`

- `F` — 女性
- `M` — 男性

## 方法版本

CKD-EPI肌酐2021/Inker：无种族142, min/max,κ0.7/0.9,α−0.241/−0.302；无胱抑素

## 已记录的公式

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1.200 × 0.9938年龄 × 1.012 (女性).

κ = 0.7 (女性) 或 0.9 (男性); α = −0.241 (女性) 或 −0.302 (男性). 结果单位 mL/min/1.73 m².

## 限制与适用人群

CKD-EPI2021是仅基于肌酐、用于18岁及以上成人的公式；要求血清肌酐测定值经IDMS标准化。其结果是以mL/min/1.73m²表示的估算值，并非滤过率的直接测量值。肾功能不稳定、妊娠、危重病、癌症以及非典型肌肉量或体型均可能降低其可靠性。接近决策阈值时，评估可能需要采用肌酐–胱抑素C联合估算或确认性测量。单独的G分级不能确认慢性肾脏病。不应自动将按体表面积标化的结果视为用于药物剂量计算的绝对清除率；应核对药品说明书、适用人群和所要求的方法。

## 参考文献

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

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

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

G1期：正常或高GFR


### 2

G1期：正常或高GFR


### 3

G4期：GFR严重降低

GFR < 60 持续超过3个月：慢性肾病和较高心血管风险。

