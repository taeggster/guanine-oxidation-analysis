# The Influence of Chronic Stress and Day Time on Genome-wide Guanine Oxidation

A bioinformatics pipeline for analyzing the influence of chronic stress and day time on genome-wide guanine oxidation and gene expression data using statistical methods (ANOVA), correlation analysis, and machine learning approaches (PCA, t-SNE, UMAP, MOFA) efficiently. Analyses are organized by genomic regions (CpG islands, gene bodies, promoters) and analysis type.

This project aims to
1. Identify genome-wide changes in guanine oxidation associated with chronic stress level and time of day.
2. Determine whether guanine oxidation has an epigenetic role in gene expression regulation.

## Data

This repository contains code only. The data, results and notebook outputs belong to the Laboratory of Toxicology at ETH Zurich and are not included, so paths such as `/path/to/lab_storage` are placeholders.

## Project Structure

```
.
├── .gitignore
├── README.md
├── bash/
│   ├── intersect_cpg.sh
│   ├── intersect_genebodies.sh
│   └── intersect_promoters.sh
└── jupyter_notebooks/
    ├── anova_bin.ipynb                                  # Two-way ANOVA for genomic bins
    ├── anova_rest.ipynb                                 # Two-way ANOVA for cpg islands, gene bodies and promoters
    ├── binning_genome_wide_data.ipynb                   # Getting oxidation data for genomic bins
    ├── cpg_expr.ipynb                                   # Getting expression data for cpg islands
    ├── cpg_oxid.ipynb                                   # Getting oxidation data for cpg islands
    ├── dim_reduction_bin.ipynb                          # Dimension reduction for genomic bins
    ├── dim_reduction_rest.ipynb                         # Dimension reduction for cpg islands, gene bodies and promoters
    ├── expr_global.ipynb                                # Global correlation analysis using Spearman Correlation
    ├── expr_local.ipynb                                 # Local correlation analysis for significant genes
    ├── fetch_data.ipynb                                 # Converting bed files to csv files for oxidation data per sample
    ├── get_oxid.ipynb                                   # Getting oxidation data for gene bodies and promoters
    ├── mofa.ipynb                                       # Global correlation analysis using MOFA
    ├── obtaining_gene_promoter_CpG_island_coordinates.ipynb
    ├── parsing_gene_bounds.ipynb
    ├── random_forest_bin.ipynb                          # Random Forest for genomic bins
    ├── random_forest_rest.ipynb                         # Random Forest for cpg islands, gene bodies and promoters
    ├── sig_intersection.ipynb                           # Intersecting significant features (genomic bins, cpg islands) with gene bodies and promoters
    ├── xgboost_bin.ipynb                                # XGBoost for genomic bins
    └── xgboost_rest.ipynb                               # XGBoost for cpg islands, gene bodies and promoters
```

