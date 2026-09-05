🧩 R Packages and Dependencies

This project uses several R packages for single-cell RNA-seq quality control, ambient RNA correction, doublet/empty-droplet assessment, visualization, integration, and downstream analysis.

📦 Required Packages

The following packages are used in this analysis:

library(Seurat)
library(SoupX)
library(EmptyNN)
library(decontX)
library(SingleCellExperiment)

library(tidyverse)
library(Nebulosa)
library(ggplot2)
library(scCustomize)
library(harmony)

set.seed(2702)

🛠️ Installation
CRAN Packages

Install the following packages from CRAN:

install.packages("Seurat")
install.packages("SoupX")
install.packages("tidyverse")
install.packages("ggplot2")
install.packages("scCustomize")
install.packages("harmony")

Bioconductor Packages

SingleCellExperiment, decontX, and Nebulosa are available through Bioconductor.

First install BiocManager:

if (!requireNamespace("BiocManager", quietly = TRUE)) {
  install.packages("BiocManager")
}


Then install the Bioconductor packages:

BiocManager::install("SingleCellExperiment")
BiocManager::install("decontX")
BiocManager::install("Nebulosa")

EmptyNN

Install EmptyNN from GitHub:

install.packages("remotes")

remotes::install_github("powellgenomicslab/EmptyNN")

🚀 Install Everything Automatically

For convenience, the following code installs the required packages only if they are not already installed:

# ============================================================
# INSTALL REQUIRED R PACKAGES
# ============================================================

# ----------------------------
# CRAN packages
# ----------------------------

cran_packages <- c(
  "Seurat",
  "SoupX",
  "tidyverse",
  "ggplot2",
  "scCustomize",
  "harmony",
  "remotes"
)

for (pkg in cran_packages) {
  if (!requireNamespace(pkg, quietly = TRUE)) {
    install.packages(pkg)
  }
}


# ----------------------------
# Bioconductor
# ----------------------------

if (!requireNamespace("BiocManager", quietly = TRUE)) {
  install.packages("BiocManager")
}

bioc_packages <- c(
  "SingleCellExperiment",
  "decontX",
  "Nebulosa"
)

for (pkg in bioc_packages) {
  if (!requireNamespace(pkg, quietly = TRUE)) {
    BiocManager::install(pkg)
  }
}


# ----------------------------
# EmptyNN from GitHub
# ----------------------------

if (!requireNamespace("EmptyNN", quietly = TRUE)) {
  remotes::install_github("powellgenomicslab/EmptyNN")
}


# ============================================================
# LOAD PACKAGES
# ============================================================

library(Seurat)
library(SoupX)
library(EmptyNN)
library(decontX)
library(SingleCellExperiment)

library(tidyverse)
library(Nebulosa)
library(ggplot2)
library(scCustomize)
library(harmony)


# ============================================================
# SET RANDOM SEED
# ============================================================

set.seed(2702)

🔗 Package Documentation and Repositories
Package	Purpose	Source
Seurat	Single-cell analysis and visualization	Seurat

SoupX	Ambient RNA contamination correction	SoupX

EmptyNN	Empty droplet identification	EmptyNN
decontX	Cell-level contamination estimation	decontX

SingleCellExperiment	Data structure for single-cell data	SingleCellExperiment

tidyverse	Data manipulation and visualization	tidyverse

Nebulosa	Density-based visualization of single-cell data	Nebulosa

ggplot2	Data visualization	ggplot2

scCustomize	Single-cell visualization and analysis utilities	scCustomize

Harmony	Batch correction and data integration	Harmony
📋 Package Installation Sources

The packages are obtained from three main sources:

CRAN
Seurat
SoupX
tidyverse
ggplot2
scCustomize
harmony
remotes

Bioconductor
SingleCellExperiment
decontX
Nebulosa

GitHub
EmptyNN

🔬 Reproducibility

A fixed random seed is used throughout the analysis to improve reproducibility:

set.seed(2702)


The same seed should be used when reproducing stochastic steps of the analysis.



