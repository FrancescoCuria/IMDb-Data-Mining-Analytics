# IMDb Data Mining Analytics

## Overview
This repository contains a comprehensive Data Mining pipeline based on a subset of the **IMDb database** (approx. 22,000 records). The project focuses on core Data Engineering tasks, including data cleansing, transformation, unsupervised segmentation, and pattern extraction to discover hidden associations between media attributes.

## Project Workflow & Architecture

### 1. Data Transformation Pipeline
* **Data Cleansing**: Handled missing values, standardized text columns, and performed rigorous data casting.
* **Feature Engineering & Selection**: Created new analytical features and performed targeted feature elimination based on correlation matrices.
* **Transformation**: Applied outlier handling and categorical encoding to prepare the tabular dataset for algorithmic ingestion.

### 2. Unsupervised Learning (Clustering)
Segmented the IMDb titles based on structural similarities using various algorithms:
* K-Means & Bisecting K-Means
* DBSCAN (Density-based spatial clustering)
* Hierarchical Clustering

### 3. Predictive Modeling (Classification & Regression)
* Built supervised models (Binary/Multiclass Classification) to categorize titles into target classes.
* Developed Multivariate Regression models to predict continuous variables such as rating counts.

### 4. Pattern & Association Rule Mining
* Extracted **Frequent Itemsets** to discover common combinations of features (e.g., genre pairings by country).
* Generated **Association Rules** to mathematically describe relationships and predict target variables based on hidden dataset patterns.

## Tech Stack
* **Language**: Python
* **Data Processing & Transformation**: Pandas, NumPy
* **Machine Learning**: Scikit-Learn
* **Data Visualization**: Matplotlib, Seaborn
