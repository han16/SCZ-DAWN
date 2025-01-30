# Purpose 
This repository contains the data and code for all analysis, for the paper "Integrating rare variant genetics and brain transcriptome data implicates novel schizophrenia putative risk genes".

# Data 

* `newGenexp.RData`, downloaded from [here](https://github.com/linnykos/covarianceSelection/blob/master/newGenexp.RData).


# Running the analysis

Just run `main_code.Rmd` to get the DAWN risk genes, with all accompanion codes in the folder. These codes are borrowed and modified from the paper [Covariance-Based Sample Selection for Heterogeneous Data: Applications to Gene Expression and Autism Risk Gene Detection](https://www.tandfonline.com/doi/full/10.1080/01621459.2020.1738234), with [codes](https://github.com/linnykos/covarianceSelection/tree/master).  

The followings are the main procedure to run the  `main_code.Rmd`. 
 
 ## load and preprocess brainspan data

* load  and clean brainspan gene expression data

## read into SCHEMA p values   

* load SCHEMA p values

## find relevant spatio-temporal BrainSpan data 

* extract relevant region/stages in brain span data, remove partitions with less than 5 samples

## run screening step 

 * set p value threshold 0.1; total number of 3,100 genes; choose 10-19 PCW data 

* in this screening step, p value of 0.01 was used, resulting in 193 genes, and the rest 2907 genes were selected with strong correlations with these 193 genes.

## Choosing tuning parameters 

* to determine the adjacency matrix, the tuning parameter $\lambda=0.24$ was used that maimizes $R^2$, by the scale free criterion.

 ## Run HMRF 
  
* one key parameter is the initial risk genes to run HMRF. We chose 15 genes with de novo mutations as initial risk genes since de novo mutations tend to be deleterious.

* with FDR at 5%, 47 genes are implicated by DAWN. 
