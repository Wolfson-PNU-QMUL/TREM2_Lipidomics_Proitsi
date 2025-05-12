WGCNA Analysis for BA9 and HC Regions followed by Module Preservation 
These scripts are for performing two related analyses: Weighted Gene Co-expression Network Analysis (WGCNA) to identify co-expression modules in gene expression data from two brain regions, BA9 (Brodmann area 9) and HC (hippocampus) in AD patient donors with TREM2 rare variants, in AD patient donors without TREM2 rare variants, and in control donors, and a module preservation analysis between these regions. The analyses aim to identify potential biomarkers, therapeutic targets, and to study the preservation of metabolite modules across these regions.

Overview
WGCNA Analysis
The WGCNA analysis identifies co-expression modules from gene expression data from BA9 and HC. The analysis also explores the association of these modules with clinical traits to identify potential biomarkers or therapeutic targets. The steps involved include data preprocessing, network construction, module detection, and exploration of the relationships between modules and clinical traits.

Module Preservation Analysis
This analysis calculates and visualizes the preservation of metabolite modules between the BA9 and HC regions. Using the WGCNA package, the preservation of modules from one region is assessed in relation to the other, helping to determine whether certain modules are conserved across both regions.

Files Included
WGCNA Analysis Files
data_res.BA9: Gene expression data for BA9 region.

data_res.HC: Gene expression data for HC region.

CovarsToUse_BA9: Clinical data for the BA9 region.

CovarsToUse_HC: Clinical data for the HC region.

Output visualizations: Dendrograms, heatmaps, and boxplots showing the relationships between modules and clinical traits.

Module Preservation Analysis Files
modulePreservationBA9L-HC.RData: The saved results from the module preservation analysis between BA9 and HC.

Metab_Module_groups_and MM.BA9.csv: The metabolite-module group data for the BA9 region.

Metab_Module_groups_and MM.HC.csv: The metabolite-module group data for the HC region.

Module_preservation_FULL.NEW.pdf: The combined plot of module preservation results.

Key Steps in the Analysis
WGCNA Analysis
Preprocessing & Quality Control: Check for missing values, outliers, and relationships between samples and clinical traits.

Network Construction: Build a co-expression network based on gene expression data using a soft-thresholding approach.

Module Detection: Identify co-expression modules through hierarchical clustering and dynamic tree cutting. Merge modules based on their eigengene dissimilarity.

Module-Trait Association: Correlate module eigengenes with clinical traits to find significant associations.

Visualization: Use boxplots to visualize the relationship between modules and clinical traits.

Regression: Fit linear regression models to explore the impact of clinical traits on module eigengenes.

Module Preservation Analysis
Data Preparation: Load the metabolite-module group data for BA9 and HC regions.

Module Preservation Calculation: Use the modulePreservation function to calculate preservation statistics for modules in both regions.

Visualization: Generate scatter plots showing the relationship between module size and preservation statistics (e.g., medianRank and Zsummary).

Prerequisites
The following R packages are required for both analyses:

WGCNA: For Weighted Gene Co-expression Network Analysis and network construction.

reshape2: For reshaping data for visualization.

ggplot2: For generating high-quality visualizations.

cowplot: For combining multiple plots into one.


Output
WGCNA Analysis Output
Network Construction: Adjacency matrices, TOM matrices, and dendrograms for both BA9 and HC regions.

Modules: Identified co-expression modules and their eigengenes.

Module-Trait Relationships: Results from the correlation of module eigengenes with clinical traits.

Visualizations: Dendrograms, heatmaps, boxplots, and plots showing the relationships between modules and clinical traits.

Regression Results: P-values from linear regression models showing the relationship between clinical traits and module eigengenes.

Module Preservation Analysis Output
PDF File: Module_preservation_FULL.NEW.pdf containing the combined preservation plots for BA9 and HC.

Preservation Statistics: medianRank and Zsummary for each module in both regions.

Visualizations: Scatter plots showing module size vs. preservation statistics (median rank and Zsummary) for BA9 and HC regions.

Results
WGCNA Results
Module-Trait Associations: Identified relationships between modules and clinical traits, potentially highlighting biomarkers or therapeutic targets.

Visualization: Various visualizations, including dendrograms, heatmaps, and boxplots, to assess the module-trait relationships.

Module Preservation Results
Module Preservation Statistics: Preservation of modules between BA9 and HC regions, measured by medianRank and Zsummary values.

Visualization: Combined figure showing plots of module size vs. preservation statistics for both BA9 and HC regions.

