<!-- ELUCENIA technical documentation · tfg-ckd-epi · de · no clinical/professional/rights approval -->

# Glomeruläre Filtrationsrate (CKD-EPI 2021)

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/tfg-ckd-epi)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Serumkreatinin

`cr`

mg/dL · Bereich: 0,2–20

### Alter

`idade`

Jahre · Bereich: 18–110

### Geschlecht

`sexo`

- `F` — Weiblich
- `M` — Männlich

## Fassung der Methode

CKD-EPI Kreatinin 2021/Inker:rassenfrei 142, min/max,κ0,7/0,9,α−0,241/−0,302; kein Cystatin

## Dokumentierte Formel

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1,200 × 0,9938Alter × 1,012 (Frauen).

κ = 0,7 (Frauen) oder 0,9 (Männer); α = −0,241 (Frauen) oder −0,302 (Männer). Ergebnis in mL/min/1,73 m².

## Grenzen und Population

Die ausschließlich auf Kreatinin beruhende CKD-EPI 2021-Gleichung ist für Erwachsene ab 18 Jahren vorgesehen; sie erfordert IDMS-standardisiertes Serumkreatinin. Sie liefert einen Schätzwert in mL/min/1,73 m² und keine direkte Messung der Filtration. Eine instabile Nierenfunktion, Schwangerschaft, kritische Erkrankung, Krebs sowie atypische Muskelmasse oder Körpermaße können ihre Zuverlässigkeit vermindern. Nahe einem Entscheidungsschwellenwert kann eine Kreatinin–Cystatin C-Schätzung oder eine bestätigende Messung erforderlich sein. Die G-Kategorie allein bestätigt keine chronische Nierenkrankheit. Der indexierte Wert darf für die Arzneimitteldosierung nicht automatisch als absolute Clearance behandelt werden; prüfen Sie Fachinformation, Patientengruppe und vorgeschriebene Methode.

## Referenzen

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
