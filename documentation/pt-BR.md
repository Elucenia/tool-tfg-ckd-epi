<!-- ELUCENIA technical documentation · tfg-ckd-epi · pt-BR · no clinical/professional/rights approval -->

# Taxa de filtração glomerular (CKD-EPI 2021)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/tfg-ckd-epi)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Creatinina sérica

`cr`

mg/dL · intervalo: 0,2–20

### Idade

`idade`

anos · intervalo: 18–110

### Sexo

`sexo`

- `F` — Feminino
- `M` — Masculino

## Edição do método

CKDEPIcreatinina 2021/Inker:semraça 142, min/max,κ0,7/0,9,α−0,241/−0,302; semcistatina

## Fórmula documentada

TFG = 142 × mín(Cr/κ, 1)α × máx(Cr/κ, 1)−1,200 × 0,9938idade × 1,012 (mulheres).

κ = 0,7 (mulheres) ou 0,9 (homens); α = −0,241 (mulheres) ou −0,302 (homens). Resultado em mL/min/1,73 m².

## Limites e população

Equação CKD-EPI2021 baseada apenas em creatinina para adultos de 18 anos ou mais; requer creatinina sérica padronizada por IDMS. É uma estimativa em mL/min/1,73m², não uma medida direta da filtração. Função renal instável, gestação, doença crítica, câncer e massa muscular ou tamanho corporal atípicos podem reduzir sua confiabilidade. Próximo a um limiar decisório, a avaliação pode requerer creatinina–cistatinaC ou medida confirmatória. A categoria G isolada não confirma DRC. O resultado indexado não deve ser tratado automaticamente como clearance absoluto para dose de medicamento; confira a bula, a população e o método exigido.

## Referências

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

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

Estágio G1: TFG normal ou alta


### 2

Estágio G1: TFG normal ou alta


### 3

Estágio G4: TFG gravemente diminuída

TFG < 60 por mais de 3 meses: doença renal crônica e alto risco cardiovascular.

