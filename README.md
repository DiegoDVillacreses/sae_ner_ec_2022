# 🇪🇨 SAE-NER: Small Area Estimation of Child Chronic Malnutrition in Ecuador

* Disclaimer: All documents were downloaded from the official INEC Ecuador website on April 4, 2025: https://www.ecuadorencifras.gob.ec/documentos/web-inec/Bibliotecas/Libros/cuadernos_trabajo/DocumentoMetodológico_SaeNerDci.pdf.

This repository contains R functions and examples developed for the project **"An Approach to Small Area Estimation of Child Chronic Malnutrition in Ecuador"**, authored by Diego Villacreses and Domingo Morales. The methodology implements **Nested Error Regression (NER)** models with **Empirical Best Prediction (EBP)** to estimate the prevalence of chronic malnutrition in children at the **canton level** using survey and census data.

> ⚠️ **Note:** Due to data privacy policies, this repository includes only code examples. No datasets are provided.

---

## 🧠 Core Methodology

We use Small Area Estimation (SAE) techniques via the **NER model**, with enhancements including:

- **Empirical Best Prediction (EBP)**
- **Bootstrap Mean Squared Error (MSE) estimation**
- **Conformity condition (benchmarking)**
- **Variable selection via Adaptive Elastic-Net**

---

## 📦 Functions

The repository includes custom R functions to perform:

- `ner_ebp_n1()` / `ner_ebp_nG()` – Estimate EBP for domains with/without survey data.
- `NER_boots()` – Bootstrap MSE for EBPs.
- `ner_ebp_nG_CC()` – Benchmarking EBPs using a conformity constraint.
- `NER_boots_CC()` – Bootstrap MSE under conformity.
- `step_AIC_glmm.forw.dv()` – Forward stepwise selection using AIC/BIC.
- `glmm_all_txs()` – Evaluate GLMMs across covariate sets.

---

## 🛠️ Tools & Dependencies

```r
library(data.table)
library(lme4)
library(magrittr)
library(doSNOW)
library(purrr)
library(stringr)
library(foreach)
```

---
