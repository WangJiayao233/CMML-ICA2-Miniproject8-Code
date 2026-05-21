# CMML-ICA2-Miniproject8-Code
# ICA2 Miniproject 8: Ambient RNA benchmarking

This repository contains code and selected outputs for ICA2 Miniproject 8, benchmarking ambient RNA correction methods in PBMC single-cell RNA-seq data.

## Overview

PBMC4K single-cell RNA-seq data were preprocessed using Seurat. Controlled ambient RNA contamination was simulated from a monocyte-like source cluster across two ambient-gene profiles and four contamination levels. DecontX and SoupX were benchmarked using ground-truth contamination fractions, count recovery, marker leakage and clustering stability. CellBender was attempted on PBMC4K raw H5 input but excluded from quantitative benchmarking because checkpoint serialization failed before H5 output generation.

## Main analysis file

- `ICA2_MP8_analysis.Rmd`

## Key figures

- `figures/FigS14_DecontX_SoupX_correction_comparison.png`
- `figures/FigS15_DecontX_SoupX_clustering_ARI.png`
- `figures/FigS11_DecontX_detection_across_scenarios.png`

## Key result tables

- `results/decontx/decontx_report_table.csv`
- `results/soupx/soupx_metrics.csv`
- `results/main_method_table.csv`
- `results/method_status_table.csv`

## Software

Main analysis was performed in R using Seurat, Matrix, celda, SoupX, mclust, ggplot2 and patchwork. CellBender was attempted using Python 3.10, CellBender 0.3.2, torch 2.1.2 and numpy 1.26.4.
