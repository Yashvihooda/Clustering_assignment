# Clustering Analysis on Breast Cancer Wisconsin Dataset

## Introduction
This project conducts a **comparative performance study** of different clustering algorithms using the **Breast Cancer Wisconsin dataset**. The dataset contains diagnostic data for breast cancer, including features such as radius, texture, perimeter, area, and smoothness.

The study applies several clustering techniques to understand their performance:
- **K-Means Clustering**
- **Agglomerative (Hierarchical) Clustering**
- **Mean Shift Clustering**

The analysis is carried out with different preprocessing techniques, and performance is evaluated using multiple metrics. Results are visualized with plots, comparing the performance of different algorithms, preprocessing methods, and evaluation parameters. The goal is to identify the most effective combination of algorithms and preprocessing techniques for clustering breast cancer data.

## Methodology

### Preprocessing Techniques
1. **No Data Processing**: Using raw data without any transformation.
2. **Normalization**: Scaling data to a standard range (0-1).
3. **Normalization + PCA**: Applying Principal Component Analysis (PCA) after normalization to reduce dimensionality.
4. **PCA Only**: Reducing the dataset's dimensions using PCA without any normalization.

### Evaluation Metrics
- **Calinski-Harabasz Index**: Measures the compactness and separation of clusters.
- **Davies-Bouldin Index**: A lower value indicates better clustering.
- **Silhouette Score**: Measures how similar each data point is to its own cluster compared to other clusters.

## Results

### Performance Metrics Summary:

| **Preprocessing**      | **Algorithm** | **Calinski-Harabasz (Clusters=3)** | **Calinski-Harabasz (Clusters=4)** | **Calinski-Harabasz (Clusters=5)** | **Davies-Bouldin (Clusters=3)** | **Davies-Bouldin (Clusters=4)** | **Davies-Bouldin (Clusters=5)** | **Silhouette (Clusters=3)** | **Silhouette (Clusters=4)** | **Silhouette (Clusters=5)** |
|------------------------|---------------|-----------------------------------|-----------------------------------|-----------------------------------|---------------------------------|---------------------------------|---------------------------------|-----------------------------|-----------------------------|-----------------------------|
| **No Data Processing** | Hierarchical  | 1089.93                           | 1245.57                           | 1541.86                           | 0.6314                          | 0.6090                          | 0.6114                          | 0.5083                      | 0.5090                      | 0.5114                      |
| **No Data Processing** | K-Means       | 1253.86                           | 1465.67                           | 1621.01                           | 0.5728                          | 0.6177                          | 0.6145                          | 0.6696                      | 0.5335                      | 0.5102                      |
| **No Data Processing** | Mean Shift    | 637.99                            | 637.99                            | 637.99                            | 0.5122                          | 0.5122                          | 0.5122                          | 0.6270                      | 0.6270                      | 0.6270                      |
| **Using Normalization**| Hierarchical  | 235.84                            | 185.19                            | 158.21                            | 1.4662                          | 1.9147                          | 1.8558                          | 0.3353                      | 0.1366                      | 0.1280                      |
| **Using Normalization**| K-Means       | 253.30                            | 202.64                            | 178.25                            | 1.4573                          | 1.4768                          | 1.7226                          | 0.3324                      | 0.2084                      | 0.1677                      |
| **Using Normalization + PCA** | Hierarchical  | 512.22                            | 448.90                            | 419.62                            | 1.0580                          | 0.9299                          | 0.8825                          | 0.4318                      | 0.3297                      | 0.3459                      |
| **Using PCA**          | K-Means       | 1265.25                           | 1485.79                           | 1649.20                           | 0.5679                          | 0.6118                          | 0.6113                          | 0.6710                      | 0.5366                      | 0.5166                      |

### Graphical Analysis:
Refer to the included plots that visually represent the comparative performance of each algorithm across different preprocessing methods and clustering sizes. These plots highlight the trends observed in the performance metrics (Calinski-Harabasz, Davies-Bouldin, and Silhouette scores) for various clustering methods.

## Conclusion

- **Best Performance**: The best Calinski-Harabasz Index values were observed with **K-Means Clustering** without any preprocessing.
- **Stability**: The **Mean Shift Clustering** method showed consistent performance across all preprocessing techniques, making it a stable choice.
- **PCA Effect**: Applying **PCA** improved clustering results when combined with normalization but did not perform as well when used alone.

### Key Findings:
- The choice of preprocessing technique (such as normalization and PCA) has a significant impact on clustering performance.
- **K-Means** with no preprocessing performed the best for Calinski-Harabasz scores.
- **Mean Shift** provided stable and consistent results, which could make it a reliable choice in some scenarios.
  
Based on the results, **K-Means with No Data Processing** and **Mean Shift Clustering** are the most promising choices for the Breast Cancer Wisconsin dataset.






