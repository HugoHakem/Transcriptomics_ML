# Transcriptomics_ML
This project compare different clustering and classifying techniques on Peripheral blood mononuclear cells transcriptomics data


<h1><center> BioE245 Final project Part1: Lower-dimension representations of the cells </h1></center>
<h2><center> Efficacy Comparison in term of clustering of AutoEncoder, PCA, tSNE for 2D representation of Peripheral blood mononuclear cells using transcriptomics data  </h2></center>
    
## Hugo Hakem Meng BioE 23-24'

### Acknowledgement
This work stands as the final project for the BioE245 class taught in Spring2024 by Professor. Liana Lareau, and GSIs. Michael Herschl, Amy Lu.

# 0) Some background and motivation
Peripheral blood mononuclear cells (PBMCs) are a group of different cell types in your blood, a subset of what we call white blood cells. They include many important parts of your immune system: T cells, B cells, natural killer cells, and so on. These cells are responsible for your innate and adaptive immune responses. When you get infected or vaccinated, they kick into high gear. In different situations, or with different diseases, the mix of different cell types shifts and so does the gene expression within one type of cell. PBMCs can be isolated very easily from patient blood samples, just by spinning the blood in a centrifuge that separates different cell types by weight. So, looking at these cells can be very informative.

For this present work, two dataset has been furnished: 
+ labels.csv stores the association between a cell barcode and a cell type label.
+ processed_counts.csv stores the normalized log read counts for each cell, where each row represents a single cell, and each column represents a gene.
    
The goal of this part of the project is to represent PBMC cells onto a 2D plot and compare the different dimensionality reduction method. 

This Notebook is partitionned as follow.
1. [Data Preprocessing](#PrePro)
2. [Model Implementation](#Model)
    1. [AutoEncoder Architecture](#AutoEncoder)
    2. [Trainer](#Trainer)
3. [2D Representation](#2Dplot)
    1. [AutoEncoder - Fine Tuning](#FineTune)
    2. [Method Comparison](#Comparison)
4. [Conclusion](#Conclusion)


To run the present Notebook, here is a list of command to run sequentially in your environment and which will install the package required. 

```conda install ipykernel conda-forge -y```
```conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia```
```conda install pandas matplotlib seaborn tqdm -c conda-forge -y```


<h1><center> BioE245 Final project Part2: Classification </h1></center>
<h2><center> Efficacy Comparison of various model for Peripheral blood mononuclear cells classification using transcriptomics data </h2></center>
    
## Hugo Hakem Meng BioE 23-24'

### Acknowledgement
This work stands as the final project for the BioE245 class taught in Spring2024 by Professor. Liana Lareau, and GSIs. Michael Herschl, Amy Lu.

# 0) Some background and motivation
Peripheral blood mononuclear cells (PBMCs) are a group of different cell types in your blood, a subset of what we call white blood cells. They include many important parts of your immune system: T cells, B cells, natural killer cells, and so on. These cells are responsible for your innate and adaptive immune responses. When you get infected or vaccinated, they kick into high gear. In different situations, or with different diseases, the mix of different cell types shifts and so does the gene expression within one type of cell. PBMCs can be isolated very easily from patient blood samples, just by spinning the blood in a centrifuge that separates different cell types by weight. So, looking at these cells can be very informative.

For this present work, two dataset has been furnished: 
+ labels.csv stores the association between a cell barcode and a cell type label.
+ processed_counts.csv stores the normalized log read counts for each cell, where each row represents a single cell, and each column represents a gene.
    
The goal of this part of the project is to classify the cell using supervised machine larning method. 

This Notebook is partitionned as follow.
1. [Data Preprocessing](#PrePro)
2. [Model Implementation](#Model)
   1. [Decision Trees](#DecTrees)
        + [XGBoost](#XGBoost)
        + [RandomForest](#RandomForest)
   2. [Bayes Model](#Bayes)
        + [Gaussian Naive Bayes](#Gaussian)
        + [Bernouilli Naive Bayes](#Bernouilli)
        + [Multivariate Gaussian Bayes](#MultiGaussian)
   3. [Feed Forward Neural Network](#FFNN)
3. [Conclusion](#Conclusion)


To run the present Notebook, here is a list of command to run sequentially in your environment and which will install the package required. 

```conda install ipykernel conda-forge -y```
```conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia```
```conda install pandas matplotlib seaborn tqdm -c conda-forge -y```
```conda install -c conda-forge py-xgboost```
    
