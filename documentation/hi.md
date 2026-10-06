<!-- ELUCENIA technical documentation · tfg-ckd-epi · hi · no clinical/professional/rights approval -->

# ग्लोमेरुलर फिल्ट्रेशन दर (CKD-EPI 2021)

[शर्तें, स्रोत और अनुमतियाँ](https://elucenia.org/hi/tools/tfg-ckd-epi)

## उपयोग कैसे करें

पोर्टल पर उपकरण का उपयोग करें या स्थानीय HTTP सर्वर के माध्यम से index.html खोलें। भाषा चुनें, फ़ील्ड भरें और गणना करें।

## इनपुट और इकाइयाँ

### सीरम क्रिएटिनिन

`cr`

mg/dL · सीमा: 0.2–20

### आयु

`idade`

वर्ष · सीमा: 18–110

### लिंग

`sexo`

- `F` — महिला
- `M` — पुरुष

## विधि का संस्करण

CKD-EPI क्रिएटिनिन 2021/Inker:बिना नस्ल 142, min/max,κ0.7/0.9,α−0.241/−0.302;बिना सिस्टैटिन

## दस्तावेज़ित सूत्र

eGFR = 142 × min(Cr/κ, 1)α × max(Cr/κ, 1)−1.200 × 0.9938आयु × 1.012 (महिला).

κ = 0.7 (महिला) या 0.9 (पुरुष); α = −0.241 (महिला) या −0.302 (पुरुष). परिणाम में mL/min/1.73 m².

## सीमाएँ और जनसमूह

CKD-EPI2021 केवल क्रिएटिनिन पर आधारित समीकरण है और 18 वर्ष या उससे अधिक आयु के वयस्कों के लिए है; इसके लिए IDMS-मानकीकृत सीरम क्रिएटिनिन चाहिए। यह mL/min/1.73m² में दिया गया अनुमान है, निस्यंदन का प्रत्यक्ष मापन नहीं। अस्थिर गुर्दा कार्य, गर्भावस्था, गंभीर रोग, कैंसर तथा असामान्य मांसपेशी मात्रा या शरीर का आकार इसकी विश्वसनीयता घटा सकते हैं। निर्णय की सीमा के निकट होने पर आकलन के लिए क्रिएटिनिन–सिस्टैटिन C का संयुक्त अनुमान या पुष्टि हेतु मापन आवश्यक हो सकता है। अकेली G श्रेणी दीर्घकालिक गुर्दा रोग की पुष्टि नहीं करती। शरीर के सतह क्षेत्रफल के लिए मानकीकृत परिणाम को दवा की खुराक के लिए अपने आप निरपेक्ष क्लियरेंस न मानें; औषधि की आधिकारिक जानकारी, लक्षित जनसमूह और आवश्यक विधि की जाँच करें.

## संदर्भ

- [Inker LA et al. New creatinine- and cystatin C–based equations to estimate GFR without race. N Engl J Med, 2021.](https://doi.org/10.1056/NEJMoa2102953)

- [KDIGO 2024 Clinical Practice Guideline for the Evaluation and Management of Chronic Kidney Disease.](https://kdigo.org/guidelines/ckd-evaluation-and-management/)

- [NIDDK adult equations, reviewedMay2025; CKD-EPI2021 creatinine variant](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/glomerular-filtration-rate-equations/adults)

- [NIDDK Clinical Measurements & eGFR Accuracy](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/factors-affecting-egfr-accuracy/clinical-measurements)

- [NIDDK drug-dosing guidance, reviewedOctober2024](https://www.niddk.nih.gov/research-funding/research-programs/kidney-clinical-research-epidemiology/laboratory/ckd-drug-dosing-providers)

## तकनीकी परीक्षण दोहराएँ

दर्ज कृत्रिम मामलों को दोहराने के लिए इस रिपॉज़िटरी की मूल निर्देशिका में node test.cjs चलाएँ। मूल इनपुट, अपेक्षित परिणाम और सहनशीलता सीमाएँ सुरक्षित रखी गई हैं। तकनीकी परीक्षण नैदानिक सत्यापन नहीं हैं।

```sh
node test.cjs
```

tool.json में स्रोत, संस्करण और समीक्षा का दायरा दिया गया है। examples.json में कृत्रिम इनपुट और अपेक्षित परिणाम सुरक्षित हैं; results.json में प्राप्त परिणाम दर्ज हैं।

[रिकॉर्ड और संदर्भ](../tool.json) · [JavaScript कोड](../calculator.js) · [संदर्भ मामले](../examples.json) · [results.json](../results.json)

## समीक्षा और उपयोग की शर्तें

स्वतंत्र नैदानिक समीक्षा नहीं की गई है।

यह इंटरफ़ेस लेखकों द्वारा किया गया अनुवाद है, कोई आधिकारिक या प्रमाणित संस्करण नहीं। स्वतंत्र नैदानिक समीक्षा, पेशेवर भाषाई समीक्षा और उपकरणों के अधिकारों की अनुमति की प्रक्रिया पूरी नहीं हुई है।

सूत्र या वर्गीकरण का परिणाम। व्याख्या, कार्यवाही और उपयुक्तता पेशेवर मूल्यांकन और चुने गए स्रोत पर निर्भर है।

## लाइसेंस और श्रेय

Apache-2.0 केवल ELUCENIA के कोड पर लागू होता है। उपकरणों, प्रकाशनों, अनुवादों और डेटा के अधिकार उनके संबंधित अधिकारधारकों के पास रहते हैं। LICENSE और NOTICE सुरक्षित रखें।

ELUCENIA · Felipe Guedes · Copyright © 2026

## दर्ज किए गए परिणाम

नीचे दी गई जानकारी कृत्रिम उदाहरणों के लिए पद्धति के आउटपुट को सुरक्षित रखती है। यह स्वतंत्र नैदानिक सत्यापन नहीं है।

### 1

चरण G1: सामान्य या उच्च GFR


### 2

चरण G1: सामान्य या उच्च GFR


### 3

चरण G4: GFR गंभीर रूप से कम

3 महीने से अधिक समय तक GFR < 60: दीर्घकालिक गुर्दे की बीमारी और उच्च हृदय-वाहिकीय जोखिम।

