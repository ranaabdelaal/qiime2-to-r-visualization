# Microbiome Data Analysis and Visualization in R

This repository contains R scripts and R Markdown notebooks for generating **publication-ready visualizations and analyses** of microbiome datasets processed with QIIME2. The workflows cover multiple aspects of microbiome data, from alpha diversity to differential pathway abundance.

The scripts assume that users have already run QIIME2 and exported the `.qza` files as tables or metadata. The repository focuses on **data import, processing, visualization, and statistical analysis in R**.

---

## Contents / Workflows

1. **Alpha Diversity Visualization**
   - Computes and plots alpha diversity metrics (Faith’s PD, Observed Features, Shannon Entropy, Pielou’s Evenness).
   - Includes boxplots with Wilcoxon rank-sum tests and multiple testing correction.
   - Outputs publication-ready figures.

2. **Beta Diversity Visualization**
   - Reads distance matrices (Bray-Curtis, Jaccard, weighted/unweighted UniFrac) exported from QIIME2.
   - Performs PERMANOVA and pairwise comparisons.
   - Generates PCoA plots with ellipses for group separation.

3. **Rarefaction Curves**
   - Plots rarefaction curves for richness (Observed Features) and diversity metrics (Shannon Entropy).
   - Visualizes sampling depth versus observed diversity per sample and group.

4. **Taxa Bar Plots**
   - Aggregates taxa at Phylum, Genus, and Species levels using `phyloseq`.
   - Highlights top taxa and groups less abundant taxa into “Other.”
   - Outputs relative abundance barplots per sample and per group.

5. **ANCOM BC (Differential Abundance)**
   - Performs differential abundance analysis using ANCOM BC results.
   - Processes log2 fold changes (LFC) and q-values.
   - Visualizes significant features with large, bold bar plots for genus/species + ASV.

6. **Differential Pathway Abundance**
   - Merges LFC and q-values with pathway annotations (e.g., MetaCyc).
   - Filters significant pathways.
   - Produces horizontal bar plots showing log2 fold change per pathway for a given comparison.

---

## Repository Structure
├── alpha_diversity/ # R Markdown and scripts for alpha diversity
├── beta_diversity/ # R Markdown and scripts for beta diversity
├── rarefaction/ # Rarefaction curve scripts
├── taxa_barplots/ # Phylum, Genus, Species relative abundance plots
├── ancom_bc/ # Differential abundance analysis scripts
├── differential_pathways/ # Pathway differential abundance scripts
├── README.md # Documentation (this file)


---

## Requirements

The following R packages are required:

- `tidyverse`  
- `ggplot2`  
- `ggpubr`  
- `qiime2R`  
- `phyloseq`  
- `vegan`  
- `RColorBrewer`  
- `purrr`  
- `stringr`  

Each script automatically checks for and installs missing packages if necessary.

---

## Usage

1. **Clone the repository**:

```bash
git clone https://github.com/ranaabdelaal/qiime2-to-r-visualization.git

