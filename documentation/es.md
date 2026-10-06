<!-- ELUCENIA technical documentation · tfg-ckd-epi · es · no clinical/professional/rights approval -->

# Tasa de filtración glomerular (CKD-EPI 2021)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/tfg-ckd-epi)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Creatinina sérica

`cr`

mg/dL · intervalo: 0,2–20

### Edad

`idade`

años · intervalo: 18–110

### Sexo

`sexo`

- `F` — Femenino
- `M` — Masculino

## Edición del método

CKD-EPI creatinina 2021/Inker:sin raza 142, min/max,κ0,7/0,9,α−0,241/−0,302; sin cistatina

## Fórmula documentada

TFGe = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1,200 × 0,9938edad × 1,012 (mujeres).

κ = 0,7 (mujeres) o 0,9 (hombres); α = −0,241 (mujeres) o −0,302 (hombres). Resultado en mL/min/1,73 m².

## Límites y población

Ecuación CKD-EPI 2021 basada únicamente en creatinina para adultos de 18 años o más; requiere creatinina sérica estandarizada mediante IDMS. Es una estimación en mL/min/1,73 m², no una medición directa de la filtración. La función renal inestable, el embarazo, la enfermedad crítica, el cáncer y una masa muscular o un tamaño corporal atípicos pueden reducir su fiabilidad. Cerca de un umbral de decisión, la evaluación puede requerir una estimación con creatinina–cistatina C o una medición confirmatoria. La categoría G por sí sola no confirma enfermedad renal crónica. El resultado indexado no debe considerarse automáticamente un aclaramiento absoluto para dosificar medicamentos; compruebe la ficha técnica, la población y el método requerido.

## Referencias

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

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

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Estadio G1: TFG normal o alta


### 2

Estadio G1: TFG normal o alta


### 3

Estadio G4: TFG gravemente disminuida

TFG < 60 durante más de 3 meses: enfermedad renal crónica y alto riesgo cardiovascular.

