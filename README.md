# Classification of Death Analysis by Risk Factors

## Project Overview

This study explores patterns in multiple health risk factors across different countries and years, from 1990 to 2019, using unsupervised learning techniques. The primary goal is to identify groups of countries with similar health risk characteristics to inform potential public health interventions. The dataset used, 'Deaths by Risk Factors 2019', was collected from 'Our World in Data' and contains 6840 rows and 31 columns, detailing deaths attributed to various health risks such as high systolic blood pressure, high BMI, high LDL cholesterol, smoking, and alcohol use.

## Methodologies

The analysis involved several key steps:

1.  **Exploratory Data Analysis (EDA)**: Initial data overview, including summary statistics and data types, was performed. Univariate analysis (histograms and density plots) described individual variable features, while bivariate analysis (scatter plots and correlation matrices) explored relationships between two variables. Multivariate analysis (pair plots and box plots) identified correlations among three or more variables. Time-series analysis was also conducted to observe data characteristics over time. Missing values were identified and handled to ensure data quality.

2.  **Unsupervised Learning**:

    **Dimensionality Reduction using Principal Component Analysis (PCA)**: PCA was applied to the scaled numerical data to reduce dimensionality while retaining variance. The principal component scores and loadings were analyzed, and a scree plot was used to determine the optimal number of principal components, revealing that the first few components captured most of the variance (e.g., the first component captured approximately 82% of the variance, and the cumulative explained variance reached about 95% around 3 to 5 components).

    **Clustering Methods**:

    * **K-means Clustering**: K-means clustering was performed on the first two principal components with 5 clusters and 10 initialization steps. Cluster labels were added to the PCA data, and clusters were plotted with their centroids.

    * **Hierarchical Clustering**: Hierarchical clustering was conducted using scaled data, the 'complete' linkage method, and Euclidean metric. A truncated dendrogram was plotted to show the top five levels of clustering. The `cut_tree` function was used to define 5 clusters and obtain cluster labels.
  

## Exploratory Data Analysis

1. Univariate Analysis

   <img width="506" height="373" alt="image" src="https://github.com/user-attachments/assets/702dc40a-31c7-49e1-8025-4cb7bebe0196" />


2. Death over time for Specific Causes

   <img width="494" height="259" alt="image" src="https://github.com/user-attachments/assets/164f47a5-e7a2-4042-96db-67caa024d0f8" />

   <img width="496" height="263" alt="image" src="https://github.com/user-attachments/assets/86e166a2-89e3-4054-b624-10015bb4f275" />



3. Bivariate Analysis

   Correlation Matrix

   <img width="470" height="359" alt="image" src="https://github.com/user-attachments/assets/bb5a62ce-cd0b-42b2-9983-9374fc015b0d" />




## Results

The analysis revealed significant relationships between different health risks and provided valuable insights into their distribution across various countries.

**PCA**: The PCA effectively reduced data dimensionality, highlighting the underlying structure and variability.

   <img width="853" height="547" alt="image" src="https://github.com/user-attachments/assets/8e3ba8c2-826d-428d-8d1c-eceec3375738" />

   <img width="440" height="265" alt="image" src="https://github.com/user-attachments/assets/b6b68e9f-b39e-4395-82fd-0dfcd5deb52d" />



**K-means Clustering**: Five distinct clusters were identified, each with unique health risk profiles : 


* **Cluster 0**: Characterized by the lowest prevalence of high LDL cholesterol, smoking, and alcohol use, and the lowest BMI values, suggesting areas with fewer general health hazards.

* **Cluster 1**: Showed the highest levels across all major risk factors, including high LDL cholesterol, smoking, alcohol consumption, and high BMI, indicating regions or populations with severe health issues.

* **Cluster 2**: Exhibited intermediate levels of health hazards for the major risk variables.

* **Cluster 3**: Generally had lower values but with more variability and occasional outliers, representing areas with varying health characteristics.

* **Cluster 4**: Displayed elevated health risk factor values, though not as extreme as Cluster 1, suggesting substantial but lesser health hazards.

  <img width="853" height="547" alt="image" src="https://github.com/user-attachments/assets/5605bea4-e580-4f1c-bd2b-d7b7b1958e57" />


    
**Hierarchical Clustering**: This method also helped define groups with similar health risk characteristics. The dendrogram graphically represented the tree structure of clusters, illustrating similarities and dissimilarities between data points and clusters.

   <img width="841" height="638" alt="image" src="https://github.com/user-attachments/assets/31680341-9de0-49c3-ad79-202a7d7795c0" />


## Conclusion

This study successfully applied unsupervised learning techniques, PCA, K-means, and Hierarchical Clustering, to analyze health risk factors and identify distinct patterns across countries from 1990 to 2019. The identified clusters provide actionable insights for public health, indicating regions needing intensive interventions versus those benefiting more from preventive measures. This research underscores the utility of unsupervised learning in extracting meaningful insights from complex healthcare datasets, supporting evidence-based decision-making for policymakers and healthcare providers to improve global health outcomes.

## Technologies & Libraries Used

* **Python**: Programming language used for analysis.
* **Pandas**: Data manipulation and analysis library.
* **NumPy**: Numerical computing library.
* **Scikit-learn**: Machine learning library for PCA and K-means.
* **SciPy**: Scientific computing library for hierarchical clustering.
* **Matplotlib**: Plotting library for data visualization.
* **Seaborn**: Statistical data visualization library.
