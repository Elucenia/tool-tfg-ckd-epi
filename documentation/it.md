<!-- ELUCENIA technical documentation · tfg-ckd-epi · it · no clinical/professional/rights approval -->

# Velocità di filtrazione glomerulare (CKD-EPI 2021)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/tfg-ckd-epi)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Creatinina sierica

`cr`

mg/dL · intervallo: 0,2–20

### Età

`idade`

anni · intervallo: 18–110

### Sesso

`sexo`

- `F` — Femminile
- `M` — Maschile

## Edizione del metodo

CKD-EPI creatinina 2021/Inker:senza razza 142, min/max,κ0,7/0,9,α−0,241/−0,302; senza cistatina

## Formula documentata

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1,200 × 0,9938età × 1,012 (donne).

κ = 0,7 (donne) o 0,9 (uomini); α = −0,241 (donne) o −0,302 (uomini). Risultato in mL/min/1,73 m².

## Limiti e popolazione

Equazione CKD-EPI 2021 basata solo sulla creatinina per adulti di 18 anni o più; richiede creatinina sierica standardizzata mediante IDMS. Fornisce una stima in mL/min/1,73 m², non una misura diretta della filtrazione. Funzione renale instabile, gravidanza, malattia critica, cancro e massa muscolare o dimensioni corporee atipiche possono ridurne l’affidabilità. Vicino a una soglia decisionale, la valutazione può richiedere una stima con creatinina–cistatina C o una misurazione di conferma. La categoria G da sola non conferma una malattia renale cronica. Il risultato indicizzato non deve essere trattato automaticamente come clearance assoluta per il dosaggio di un farmaco; verificare il riassunto delle caratteristiche del prodotto, la popolazione e il metodo richiesto.

## Riferimenti

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Stadio G1: GFR normale o elevato


### 2

Stadio G1: GFR normale o elevato


### 3

Stadio G4: GFR gravemente ridotta

GFR < 60 per più di 3 mesi: malattia renale cronica e alto rischio cardiovascolare.

