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

![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/b08b9ce0-edfb-4d0c-8048-a81dd8609e15)

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

![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/14744466-5f25-49e6-a6ac-aeabb6d54d02)

1. **Culmen Length Distribution**
   - The distribution of culmen length appears to be approximately normal.

2. **Culmen Depth Distribution**
   - The distribution suggests potential subgroupings within the data.

3. **Flipper Length Distribution**
   - The distribution is balanced but with multiple peaks.

4. **Body Mass Distribution**
   - The distribution of body mass is slightly right-skewed.

### Plot Correlation Heatmap

A correlation heatmap was generated to visualize the pairwise correlations between the numerical features in the dataset:

![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/b2a044d4-3a35-405d-97c1-ed0558e02b5d)

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

![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/69d114bb-19ee-47a2-804d-9aae7d4ca700)

## Hierarchical Clustering

Performed using the Ward linkage method, with the dendrogram indicating 3 clusters. Data points were assigned to clusters based on the hierarchical structure.

![image](https://github.com/Ahmed-Mostafa-88/Clustering_Penguins_Species/assets/144740078/a0986139-3f76-4291-8093-a0f0e20780fb)

## Evaluation and Interpretation

Evaluation metrics:
- **Silhouette Score**: Indicates moderate separation and internal cohesion of clusters.
- **Davies-Bouldin Index**: Suggests moderate separation between clusters.

Both clustering techniques showed comparable performance in segmenting the penguin dataset based on physical characteristics.

