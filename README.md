# Transcriptomics_ML

This project explores different clustering and classification techniques applied to Peripheral blood mononuclear cells (PBMCs) transcriptomics data. It is divided into two parts: dimensionality reduction and classification.

For a quick result overwiew, please refer to the pdf. 

---

## Author
Hugo Hakem, MEng BioE '23-24

## Acknowledgements
This work serves as the final project for the BioE245 class taught in Spring 2024 by **Professor Liana Lareau** and **GSIs Michael Herschl and Amy Lu**.

---

# Background and Motivation

Peripheral blood mononuclear cells (PBMCs) are a subset of white blood cells that play crucial roles in both the innate and adaptive immune systems. PBMCs include various immune cells such as T cells, B cells, and natural killer cells. These cells can be easily isolated from blood samples, making them highly informative for research purposes. Transcriptomics data from PBMCs provides valuable insights into immune responses and disease states, as changes in gene expression reflect the immune system's activity.

For this project, two datasets were provided:
- **labels.csv**: Contains the association between cell barcodes and their respective cell type labels.
- **processed_counts.csv**: Stores normalized log read counts for each cell, with rows representing cells and columns representing genes.

---

# Part 1: Dimensionality Reduction of PBMCs
## Efficacy Comparison of AutoEncoder, PCA, and t-SNE for 2D Representation

The goal of this part is to compare different dimensionality reduction techniques (AutoEncoder, PCA, and t-SNE) to represent PBMCs on a 2D plot.

### Notebook Structure:
1. [Data Preprocessing](#PrePro)
2. [Model Implementation](#Model)
   1. [AutoEncoder Architecture](#AutoEncoder)
   2. [Trainer](#Trainer)
3. [2D Representation](#2Dplot)
   1. [AutoEncoder - Fine Tuning](#FineTune)
   2. [Method Comparison](#Comparison)
4. [Conclusion](#Conclusion)

---

# Part 2: Classification of PBMCs
## Efficacy Comparison of Various Models for PBMC Classification

The goal of this part is to classify PBMCs using supervised machine learning techniques such as Decision Trees, Naive Bayes models, and Feed Forward Neural Networks.

### Notebook Structure:
1. [Data Preprocessing](#PrePro)
2. [Model Implementation](#Model)
   1. [Decision Trees](#DecTrees)
      - [XGBoost](#XGBoost)
      - [RandomForest](#RandomForest)
   2. [Bayes Models](#Bayes)
      - [Gaussian Naive Bayes](#Gaussian)
      - [Bernoulli Naive Bayes](#Bernouilli)
      - [Multivariate Gaussian Bayes](#MultiGaussian)
   3. [Feed Forward Neural Network](#FFNN)
3. [Conclusion](#Conclusion)

---

## Installation Instructions

To run both notebooks, install the following packages:

```bash
conda install ipykernel conda-forge -y
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
conda install pandas matplotlib seaborn tqdm -c conda-forge -y
conda install -c conda-forge py-xgboost
