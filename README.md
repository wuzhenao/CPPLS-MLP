# CPPLS-MLP

R package for estimating cell-cell communications from spatial transcriptome data with single-cell resolution.

# Install dependent packages
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
(1)If you want to use CPPLS to build a cell-to-cell communication network, you can decompress the 2023_01_seqFISH+.zip and 2023_01_Seq-Scope.zip packages and run them in R：

run 2023_01_seqFISH+.RMD

run 2023_01_Seq-Scope.RMD


![image](https://github.com/wuzhenao/CPPLS-MLP/assets/114455899/6ac04695-faea-430e-adcd-85056c5e8890)



(2)After building a communication network between two cells, we have integrated the cell communication network into a MIMO system. If you want to get this result, you need to unzip the compare_hvg.zip, which contains the solution for all paths for each cell, and get the MIMO system in a code file called a directed graph.


![image](https://github.com/wuzhenao/CPPLS-MLP/assets/114455899/b85da792-38e1-4144-a020-d65a50e70445)




