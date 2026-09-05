# 🧬 snRNA-Seq Liver Analysis — University of Minnesota

This repository contains an analysis of **single-nucleus RNA sequencing (snRNA-seq)** data from **mouse liver samples** collected at Young and Aged

---

## 📘 Overview

The analysis focuses on:

- Preprocessing and quality control of snRNA-seq data  
- Integration and batch correction using **Harmony**  
- Clustering and visualization of distinct liver cell populations  
- Identification of age-associated differentially expressed genes in Hepatocytes and Endothelial Cells  
- Sub-Clustering of Hepatocytes and Endothelial Cells
- Identification of Senescent Cells in Hepatocytes and Endothelial Cells
- Analysis of Identified Senescent Cells

---

## 🧩 Packages Used

```r
# ============================================================
# 1. INSTALL REQUIRED R PACKAGES
# ============================================================

# CRAN packages
install.packages("Seurat")
install.packages("tidyverse")
install.packages("ggplot2")
install.packages("scCustomize")
install.packages("harmony")

# Bioconductor package
if (!requireNamespace("BiocManager", quietly = TRUE)) {
  install.packages("BiocManager")
}

BiocManager::install("Nebulosa")


# ============================================================
# 2. LOAD REQUIRED PACKAGES
# ============================================================

library(Seurat)
library(tidyverse)
library(Nebulosa)
library(ggplot2)
library(scCustomize)
library(harmony)


# ============================================================
# 3. SET RANDOM SEED
# ============================================================

set.seed(2702)




