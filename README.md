# Clustering Penguins Species

This project explores and identifies underlying patterns and structures within a dataset containing physical characteristics of penguins using clustering techniques such as K-medoids and hierarchical clustering.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Dataset Selection](#dataset-selection)
- [Data Preprocessing](#data-preprocessing)
  - [Dropping Null Values](#dropping-null-values)
  - [Detecting Outliers and Inconsistencies](#detecting-outliers-and-inconsistencies)
  - [Scaling the Features](#scaling-the-features)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Visualize Feature Distributions](#visualize-feature-distributions)
  - [Plot Correlation Heatmap](#plot-correlation-heatmap)
  - [Summary Statistics](#summary-statistics)
- [K-medoids Clustering](#k-medoids-clustering)
- [Hierarchical Clustering](#hierarchical-clustering)
- [Evaluation and Interpretation](#evaluation-and-interpretation)

## Problem Statement

The aim of this data mining project is to explore and identify underlying patterns and structures within a dataset containing physical characteristics of penguins (culmen length, culmen depth, flipper length, body mass) along with their sex. By applying clustering techniques such as K-medoids and hierarchical clustering, the objective is to partition the penguin population into distinct groups based on their physical attributes.

## Dataset Selection

The dataset used for this project is the "Clustering Penguins Species" dataset from Kaggle, consisting of the following columns:
- `culmen_length_mm`: Length of the culmen (bill) in millimeters.
- `culmen_depth_mm`: Depth of the culmen in millimeters.
- `flipper_length_mm`: Length of the penguin's flipper in millimeters.
- `body_mass_g`: Body mass of the penguin in grams.
- `sex`: Sex of the penguin (male, female, or unknown).

## Data Preprocessing

### Dropping Null Values

We started by cleaning the data and dropping any null values.

### Detecting Outliers and Inconsistencies

We applied Winsorization to numerical columns, capping the bottom and top 5% of the data values to limit the effect of outliers. Boxplots were generated for each numerical feature to identify potential outliers, but no significant outliers were observed.

### Scaling the Features

Features were scaled to bring all values to a similar scale, ensuring that no single feature dominated the clustering process.

## Exploratory Data Analysis (EDA)

### Visualize Feature Distributions

Histograms were plotted to visualize the distributions of each numerical feature:

1. **Culmen Length Distribution**
   - ![Culmen Length Distribution](![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/c67fbb2c-f9c6-4c3e-84c3-5bfdaf5c9b80)
)
   - The distribution of culmen length appears to be approximately normal.

2. **Culmen Depth Distribution**
   - ![Culmen Depth Distribution](path/to/culmen_depth_distribution.png)
   - The distribution suggests potential subgroupings within the data.

3. **Flipper Length Distribution**
   - ![Flipper Length Distribution](path/to/flipper_length_distribution.png)
   - The distribution is balanced but with multiple peaks.

4. **Body Mass Distribution**
   - ![Body Mass Distribution](path/to/body_mass_distribution.png)
   - The distribution of body mass is slightly right-skewed.

### Plot Correlation Heatmap

A correlation heatmap was generated to visualize the pairwise correlations between the numerical features in the dataset:
- ![Correlation Heatmap](path/to/correlation_heatmap.png)
- **Key Insights**:
  - Strong positive correlation between flipper length and body mass.
  - Moderate positive correlations between culmen length with flipper length and body mass.
  - Weak negative correlation between culmen length and culmen depth.
  - Moderate negative correlations involving culmen depth with flipper length and body mass.

### Summary Statistics

- **Mean**: Centered around zero.
- **Standard Deviation**: Close to 1.
- **Minimum and Maximum**: Represent the range of observed values.
- **Quartiles**: Provide insights into data spread and potential outliers.

## K-medoids Clustering

The optimal number of clusters was determined using the elbow method, resulting in 3 clusters. The K-medoids algorithm assigned each data point to one of these clusters based on its similarity to the medoid.

- ![Elbow Method](path/to/elbow_method.png)
- ![K-medoids Clustering](path/to/k_medoids_clustering.png)

## Hierarchical Clustering

Performed using the Ward linkage method, with the dendrogram indicating 3 clusters. Data points were assigned to clusters based on the hierarchical structure.

- ![Dendrogram](path/to/dendrogram.png)
- ![Hierarchical Clustering](path/to/hierarchical_clustering.png)

## Evaluation and Interpretation

Evaluation metrics:
- **Silhouette Score**: Indicates moderate separation and internal cohesion of clusters.
- **Davies-Bouldin Index**: Suggests moderate separation between clusters.

Both clustering techniques showed comparable performance in segmenting the penguin dataset based on physical characteristics.

