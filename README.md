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


(3)Based on the HVGs involved in the construction of the MIMO system, we extracted the HVGs on the dataset based on four methods: FindVariableFeatures(), variance, scannpy, and M3drop. If you want to reproduce this result, you can get the specific code in the folder where the HVG was extracted from the compare_hvg.zip, so that you can.

(4)Based on the query information, we wrote a code that could better apply all the genes to find out if the gene was involved in cellular communication under our criteria：

Enter the list of genes and then run the search_gene to get the results under this criterion.

(5)Finally, you can get the comparison result between CPPLS-MLP and CCPLS in the Kernel function comparison.zip.

(6)If you want to reproduce the results of MLP's classification of genes, you can get it in the divide folder：

run  Seqfish+_Find_var.ipynb

run  Seqfish+_Find_var.ipynb

![image](https://github.com/wuzhenao/CPPLS-MLP/assets/114455899/1b48e576-b188-4536-9c0c-c44df773ea31)


If you are interested in replicating our methods and have questions, please contact us by email. Email: 2285308398@qq.com. We welcome your criticism and correction of our methods.
