# Alpha Diversity Visualization in R

This repository contains R scripts for generating **publication-ready visualizations** of alpha diversity metrics (e.g., Faith's PD, Observed Features, Shannon Entropy, Pielou's Evenness) from **QIIME2-exported data**.  

The code assumes that users have already run QIIME2 and exported the `.qza` files into `.tsv` tables. These scripts focus only on the visualization and statistical analysis steps in R.

---

## Features
- Import QIIME2-exported alpha diversity metrics and sample metadata
- Merge alpha diversity values with metadata
- Generate boxplots with significance testing (Wilcoxon rank-sum test)
- Calculate summary statistics (mean ± SD)
- Perform pairwise statistical comparisons with multiple testing correction
- Customize plot appearance and export high-resolution figures
---

## Repository Structure
- `alpha_diversity_visualization.R` – main R script with workflow  
- `README.md` – documentation (this file)  

---

## Requirements
The following R packages are required:
- `tidyverse`
- `ggpubr`

The script automatically installs missing packages when first run.

---

## Usage

1. **Clone this repository**:
   ```bash
   git clone https://github.com/ranaabdelaal/alpha-diversity-visualization.git
