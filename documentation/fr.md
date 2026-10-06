<!-- ELUCENIA technical documentation · tfg-ckd-epi · fr · no clinical/professional/rights approval -->

# Débit de filtration glomérulaire (CKD-EPI 2021)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/tfg-ckd-epi)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Créatinine sérique

`cr`

mg/dL · intervalle: 0,2–20

### Âge

`idade`

ans · intervalle: 18–110

### Sexe

`sexo`

- `F` — Féminin
- `M` — Masculin

## Édition de la méthode

CKD-EPI créatinine 2021/Inker:sans race 142, min/max,κ0,7/0,9,α−0,241/−0,302; sans cystatine

## Formule documentée

DFGe = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1,200 × 0,9938âge × 1,012 (femmes).

κ = 0,7 (femmes) ou 0,9 (hommes); α = −0,241 (femmes) ou −0,302 (hommes). Résultat en mL/min/1,73 m².

## Limites et population

Équation CKD-EPI 2021 fondée uniquement sur la créatinine pour les adultes de 18 ans ou plus ; elle nécessite une créatinine sérique standardisée par IDMS. Elle fournit une estimation en mL/min/1,73 m², et non une mesure directe de la filtration. Une fonction rénale instable, la grossesse, une maladie critique, un cancer et une masse musculaire ou une taille corporelle atypiques peuvent réduire sa fiabilité. À proximité d’un seuil décisionnel, l’évaluation peut nécessiter une estimation créatinine–cystatine C ou une mesure de confirmation. La catégorie G seule ne confirme pas une maladie rénale chronique. Le résultat indexé ne doit pas être automatiquement assimilé à une clairance absolue pour la posologie d’un médicament ; vérifiez son résumé des caractéristiques, la population et la méthode requise.

## Références

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Stade G1 : DFG normal ou élevé


### 2

Stade G1 : DFG normal ou élevé


### 3

Stade G4 : DFG sévèrement diminué

DFG < 60 pendant plus de 3 mois : maladie rénale chronique et risque cardiovasculaire élevé.

