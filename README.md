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
