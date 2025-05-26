# GCIM: a software to detect QTL and QEI in RIL, DH, BC, and F2 populations.

Within R environment, the QTL.gCIMapping v3.5 software can be installed as below. 
First install the dependency packages:
install.packages(c("data.table","doParallel","foreach","glmnet","iterators","magrittr","openxlsx","qtl","Rcpp","shape","stringi","stringr","zip","MASS","lars","readxl", "biglasso","progress","RcppEigen"))
Then install the QTL.gCIMapping_3.5 package from local files.

Once the software package QTL.gCIMapping v3.5 is installed, users may run it using two commands:
library("QTL.gCIMapping")
QTL.gCIMapping (***)

1.RIL/DH/BC population
1.1 QTL identification
QTL.gCIMapping(file="D:/Users/GCIM_Format_DH.csv",Population="DH",method="GCIM",WalkSpeed=1,CriLOD=2.5,Trait=1,dir="D:/Users")

1.2 QEI identification (3vGCIM)
QTL.gCIMapping(fileGen="D:/Users/fileGen_Multi_env_RIL.csv",filePhe="D:/Users/filePhe_Multi_env_RIL.csv",method="Multi_env_RIL",fixedModel=FALSE,Marker_Space_Type="Position",Geno_Type=c("A","H"), Trait=1,n.en=3,dir="D:/Users/")

2.F2 population
2.1 QTL identification
QTL.gCIMapping(file="D:/Users/GCIM_Format_F2.csv",Population="F2",method="GCIM",WalkSpeed=1,CriLOD=2.5,Trait=1,dir="D:/Users")

2.2 QEI identification
QTL.gCIMapping(file="D:/Users/GCIM_Format_F2.csv",Population="F2",MultiEnv=TRUE,dir="D:/Users")

References

1	Wang Shi-Bo, Wen Yang-Jun, Ren Wen-Long, Ni Yuan-Li, Zhang Jin, Feng Jian-Ying, Zhang Yuan-Ming*. Mapping small-effect and linked quantitative trait loci for complex traits in backcross or DH populations via a multi-locus GWAS methodology. Scientific Reports 2016, 6: 29951.

2	Wen Yang-Jun, Zhang Ya-Wen, Zhang Jin, Feng Jian-Ying, Jim M. Dunwell, Zhang Yuan-Ming*. An efficient multi-locus mixed model framework for the detection of small and linked QTLs in F2. Briefings in Bioinformatics 2019, 20(5): 1913-1924.

3	Zhang Ya-Wen, Wen Yang-Jun, Jim M. Dunwell, Zhang Yuan-Ming*. QTL.gCIMapping.GUI v2.0: An R software for detecting small-effect and linked QTLs for quantitative traits in bi-parental segregation populations. Computational and Structural Biotechnology Journal 2020, 18: 59-65.

4	Wen Yang-Jun, Zhang Ya-Wen, Zhang Jin, Feng Jian-Ying, Zhang Yuan-Ming*. The improved FASTmrEMMA and GCIM algorithms for genome-wide association and linkage studies in large mapping populations. The Crop Journal 2020, 8(5): 723-732.

5	Zhou Ya-Hui, Li Guo, Zhang Yuan-Ming*. A compressed variance component mixed model framework for detecting small and linked QTL-by-environment interactions. Briefings in Bioinformatics 2021, 23(2): bbab596.

6	Li Mei, Zhang Yuan-Ming*. 3vGCIM: a compressed variance component mixed model for detecting QTL-by-environment interactions in RIL population. Journal of Genetics and Genomics 2025, in revision.
