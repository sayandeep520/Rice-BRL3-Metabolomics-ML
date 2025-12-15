
# Metabolomics Data Analysis with AI-driven Imputation and Biomarker Discovery

This Google Colab notebook provides a comprehensive workflow for analyzing metabolomics data, from raw data loading and AI-driven imputation to advanced biomarker discovery and mechanistic hypothesis generation.

## Workflow Phases:

1.  **Data Preprocessing & Imputation:**
    *   Loads raw metabolomics intensity and sample metadata.
    *   Merges dataframes and performs initial cleaning.
    *   Utilizes **SAITS (Self-Attention-based Time Series Imputation)**, an AI model, to accurately fill in missing data points.
    *   Visualizes missingness before and after imputation.

2.  **Biomarker Identification:**
    *   Generates **Volcano Plots** to identify significantly differentially expressed metabolites between experimental groups (e.g., wild-type vs. mutant).
    *   Performs **Hierarchical Clustering** to visualize patterns of significant metabolites across samples.

3.  **Deep Dive - Multivariate Analysis & Pattern Matching:**
    *   Applies **PLS-DA (Partial Least Squares Discriminant Analysis)** to identify metabolites contributing most to group separation (VIP scores).
    *   Performs "Mirror Image" analysis to pinpoint metabolites showing opposite trends in loss-of-function mutants vs. overexpression lines, suggesting direct regulatory relationships.

4.  **Pathway Enrichment Analysis:**
    *   Maps important metabolites to biological pathways to uncover enriched biological processes.

5.  **Network Analysis & Rewiring:**
    *   Constructs and visualizes **Metabolic Rewiring Networks** based on changes in metabolite-metabolite correlations between groups, highlighting altered metabolic interactions.

6.  **Advanced Validation & Hypothesis Generation:**
    *   Uses **Random Forest Classifier** to validate biomarker robustness and identify top predictive features.
    *   Performs **Bootstrapping** on VIP scores to assess biomarker stability.
    *   Infers **Direct Networks** using Graphical Lasso to identify direct metabolic interactions.
    *   Generates **Gene-Metabolite Hypotheses** based on known enzyme-metabolite relationships, providing testable predictions for wet-lab validation.

## How to Use:

1.  **Upload Data:** Ensure your `MTBLS2289_145253_compressed_files.zip` file is uploaded to your Colab environment's `/content/` directory.
2.  **Run Cells Sequentially:** Execute each code cell in order, following the phase-wise organization.
3.  **Adjust Parameters:** Pay attention to comments within cells that suggest parameters for modification (e.g., P-value and Fold Change cutoffs in Volcano Plots).
4.  **Interpret Outputs:** Review the generated plots and printed summaries for insights into your metabolomics data.

## Key Outputs:

*   Heatmaps of metabolite intensities (raw and imputed).
*   Volcano plots highlighting significant metabolites.
*   PLS-DA VIP score bar plots.
*   Pathway enrichment bar plots.
*   Box plots for mirror-image candidates.
*   Metabolic rewiring networks.
*   Random Forest feature importance plots.
*   Bootstrapped VIP score plots with confidence intervals.
*   Graphical Lasso direct network heatmaps.
*   Printouts of biological hypotheses for gene-metabolite relationships.

This notebook is designed for researchers looking to extract meaningful biological insights from complex metabolomics datasets using advanced computational and AI-driven approaches.
