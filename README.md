# CPPLS-MLP

R package for estimating cell-cell communications from spatial transcriptome data with single-cell resolution.

# Install

dependence: R version <= 4.2.3.

Install dependent packages
install.packages(c("cluster", "circlize", "dplyr", "pls", "purrr", "Seurat", "stringr"), dependencies = TRUE)
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("ComplexHeatmap")

dependence: python version >= 3.7
Install dependent packages
pip install networkx == 3.2.1
    install panda    == 2.1.0 

# run
run 2023_01_seqFISH+.RMD
run 2023_01_Seq-Scope.RMD

