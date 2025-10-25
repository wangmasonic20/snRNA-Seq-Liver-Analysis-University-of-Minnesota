# 🧬 snRNA-Seq Liver Analysis — University of Minnesota

This repository contains an analysis of **single-nucleus RNA sequencing (snRNA-seq)** data from **mouse liver samples** collected at **8 weeks (young)** and **2 years (aged)**.  
The study aims to explore age-associated transcriptional changes, cellular composition differences, and pathway alterations in the liver across the aging process.

---

## 📘 Overview

The analysis focuses on:

- Preprocessing and quality control of snRNA-seq data  
- Integration and batch correction using **Harmony**  
- Clustering and visualization of distinct liver cell populations  
- Identification of age-associated differentially expressed genes  
- Pathway enrichment and biological interpretation  

---

## 🧩 Packages Used

```r
library(Seurat)
library(tidyverse)
library(Nebulosa)
library(ggplot2)
library(scCustomize)
library(harmony)
set.seed(2702)



