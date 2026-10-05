<!-- ELUCENIA technical documentation · tfg-ckd-epi · ar · no clinical/professional/rights approval -->

# معدل الترشيح الكبيبي (CKD-EPI 2021)

[الشروط والمصادر والأذونات](https://elucenia.org/ar/tools/tfg-ckd-epi)

## كيفية الاستخدام

استخدم الأداة في البوابة أو افتح index.html عبر خادم HTTP محلي. اختر اللغة، وأكمل الحقول، ثم أجرِ الحساب.

## المدخلات والوحدات

### كرياتينين المصل

`cr`

mg/dL · النطاق: ٠٫٢–٢٠

### العمر

`idade`

سنوات · النطاق: ١٨–١١٠

### الجنس

`sexo`

- `F` — أنثى
- `M` — ذكر

## إصدار الطريقة

CKD-EPI كرياتينين 2021/Inker:دون عرق 142, min/max,κ0.7/0.9,α−0.241/−0.302؛دون سيستاتين

## المعادلة الموثقة

الترشيح المقدّر = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1.200 × 0.9938العمر × 1.012 (نساء).

κ = 0.7 (نساء) أو 0.9 (رجال); α = −0.241 (نساء) أو −0.302 (رجال). النتيجة بـ mL/min/1.73 m².

## الحدود والفئة السكانية

معادلة CKD-EPI2021 المعتمدة على الكرياتينين وحده للبالغين بعمر 18 سنة فأكثر؛ وتتطلب كرياتينين مصليًا مُعايرًا وفق معيار IDMS. إنها تقدير بوحدة mL/min/1.73m²، وليست قياسًا مباشرًا للترشيح. قد تقل موثوقيتها في حالات عدم استقرار الوظيفة الكلوية، والحمل، والمرض الحرج، والسرطان، وعندما تكون الكتلة العضلية أو حجم الجسم غير نمطيين. قرب عتبة اتخاذ قرار، قد يتطلب التقييم استخدام الكرياتينين مع السيستاتين C أو إجراء قياس تأكيدي. لا تؤكد الفئة G بمفردها وجود مرض كلوي مزمن. لا ينبغي التعامل مع النتيجة المُفهرسة بحسب مساحة سطح الجسم تلقائيًا بوصفها تصفية مطلقة لتحديد جرعة الدواء؛ تحقق من النشرة الدوائية والفئة السكانية والطريقة المطلوبة.

## المراجع

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

## إعادة إجراء الاختبارات التقنية

شغّل node test.cjs في المجلد الجذري لهذا المستودع لتكرار الحالات الاصطناعية المسجلة. تُحفظ المدخلات والنتائج المتوقعة وحدود التفاوت الأصلية. لا تُعدّ الاختبارات التقنية تحققًا سريريًا.

```sh
node test.cjs
```

يحتوي tool.json على المصادر والإصدار ونطاق المراجعة. يحتفظ examples.json بالمدخلات والنتائج المتوقعة للحالات الاصطناعية؛ ويسجل results.json النتائج التي تم الحصول عليها.

[السجل والمراجع](../tool.json) · [شيفرة JavaScript](../calculator.js) · [حالات مرجعية](../examples.json) · [results.json](../results.json)

## المراجعة وشروط الاستخدام

لم تُجرَ مراجعة سريرية مستقلة.

هذه الواجهة ترجمة أعدّها مؤلفوها، وليست إصدارًا رسميًا أو معتمدًا. لم تُجرَ مراجعة سريرية مستقلة أو مراجعة لغوية مهنية، ولم تُستكمل الموافقة على حقوق استخدام الأدوات.

نتيجة المعادلة أو التصنيف. يعتمد التفسير والتصرف ومدى الانطباق على التقييم المهني والمصدر المحدد.

## الترخيص ونسبة العمل إلى أصحابه

ينطبق Apache-2.0 على كود ELUCENIA فقط. تبقى حقوق الأدوات والمنشورات والترجمات والبيانات لأصحابها المعنيين. احتفظ بملفّي LICENSE وNOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
