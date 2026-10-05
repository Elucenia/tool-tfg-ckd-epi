<!-- ELUCENIA technical documentation · tfg-ckd-epi · en · no clinical/professional/rights approval -->

# Glomerular filtration rate (CKD-EPI 2021)

[conditions, sources and permissions](https://elucenia.org/en/tools/tfg-ckd-epi)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Serum creatinine

`cr`

mg/dL · range: 0.2–20

### Age

`idade`

years · range: 18–110

### Sex

`sexo`

- `F` — Female
- `M` — Male

## Method edition

CKD-EPI creatinine 2021/Inker:race-free 142, min/max,κ0.7/0.9,α−0.241/−0.302; no cystatin

## Documented formula

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1.200 × 0.9938age × 1.012 (women).

κ = 0.7 (women) or 0.9 (men); α = −0.241 (women) or −0.302 (men). Result in mL/min/1.73 m².

## Limits and population

The creatinine-only CKD-EPI 2021 equation is for adults aged 18 years or older and requires IDMS-standardized serum creatinine. It provides an estimate in mL/min/1.73 m², not a direct measurement of filtration. Unstable kidney function, pregnancy, critical illness, cancer and atypical muscle mass or body size may reduce its reliability. Near a decision threshold, assessment may require creatinine–cystatin C estimation or a confirmatory measurement. A G category alone does not confirm CKD. The indexed result must not automatically be treated as absolute clearance for medication dosing; check the medicine’s label, population and required method.

## References

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

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
