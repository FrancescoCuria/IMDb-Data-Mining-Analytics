# IMDb Data Mining & Analytics

## Overview
This repository contains a comprehensive Data Mining pipeline applied to a subset of the IMDb database (~22,000 records, 23 initial features). The project covers the full machine learning lifecycle, from rigorous data preprocessing and outlier handling to unsupervised segmentation (clustering), predictive modeling (classification/regression), and frequent pattern extraction.
**[Read the full Project Report (PDF)](IMDbProjectReport.pdf)**

## Project Workflow & Architecture

### 1. Data Transformation Pipeline
* **Data Cleansing**: Handled missing values, standardized text columns, and performed rigorous data casting.
* **Feature Engineering & Selection**: Created new analytical features and performed targeted feature elimination based on correlation matrices.
* **Transformation**: Applied outlier handling and categorical encoding to prepare the tabular dataset for algorithmic ingestion.

### 2. Unsupervised Learning (Clustering)
Segmented the IMDb titles based on structural similarities using various algorithms:
* K-Means & Bisecting K-Means: Identified the optimal segmentation at $k=5$ by performing feature selection.
* Hierarchical Clustering: Validated cluster compactness using Ward and Single Linkage dendrograms.
* DBSCAN (Density-based spatial clustering)

### 3. Predictive Modeling (Classification & Regression)
* Binary & Multiclass Classification: Trained K-NN, Naive Bayes, and Decision Trees.
  * Achieved F1: 0.92 and ROC-AUC: 0.96 on the isMovie binary task using an optimized Decision Tree.
  * Reached a weighted F1: 0.84 on the titleType multiclass prediction via Grid-Searched Decision Trees (Gini impurity, max depth: 10).
* Regression Analysis: Modeled user engagement (userReviewsTotal) using Linear, Ridge, Lasso, Decision Tree, and K-NN Regressors.
The best performance was achieved using a Multiple Regression approach with a K-NN Regressor ($k=20$), reaching an $R^2$ of 0.620.

### 4. Pattern & Association Rule Mining
* Discretization: Binned continuous variables into categorical ranges (e.g., SLength, HRated) to enable effective pattern discovery.
* Frequent Itemsets: Deployed Apriori and FP-Growth algorithms. Identified 73 frequent itemsets using a 0.10 support threshold.
* Association Rules: Extracted 19 highly confident rules (Confidence $\geq$ 0.6). Discovered strong, semantically meaningful associations, such as predicting high ratings (HRated) from short TV episodes (SLength, tvEpisode) with a Lift of 1.59.

## Tech Stack
* **Language**: Python
* **Data Processing & Transformation**: Pandas, NumPy
* **Machine Learning**: Scikit-Learn
* **Data Visualization**: Matplotlib, Seaborn






