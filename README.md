# Purpose 
This repository contains the data and code for all analysis, for the paper "Integrating rare variant genetics and brain transcriptome data implicates novel schizophrenia putative risk genes".

# Data 

* `newGenexp.RData`, downloaded from [here](https://github.com/linnykos/covarianceSelection/blob/master/newGenexp.RData).


# Running the analysis

Just run `main_code.Rmd` to get the DAWN risk genes, with all accompanion codes in the folder. These codes are borrowed and modified from the paper [Covariance-Based Sample Selection for Heterogeneous Data: Applications to Gene Expression and Autism Risk Gene Detection](https://www.tandfonline.com/doi/full/10.1080/01621459.2020.1738234), with [codes](https://github.com/linnykos/covarianceSelection/tree/master).  
 
 ## load and preprocess brainspan data

* load  and clean brain span gene expression data

## read into SCHEMA p values   

* load SCHEMA p values

  
 

* A total of 3100 genes were used in this analysis. In the screening step, p value of 0.01 was used, resulting in 193 genes, and the rest 2907 genes were selected with strong correlations with these 193 genes.

* To determine the adjacency matrix, the tuning parameter $\lambda=0.24$ was used that maimizes $R^2$, by the scale free criterion.
  
* One key parameter is the initial risk genes to run HMRF. We chose 15 genes with de novo mutations as initial risk genes since de novo mutations tend to be deleterious. 
