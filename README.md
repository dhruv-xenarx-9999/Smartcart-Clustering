# Code workflow

smartcart_customers.csv
          |
          v
Load data with pandas
          |
          v
Inspect and impute missing Income values
          |
          v
Feature engineering
(Age, CustomerTenureDays, TotalSpending, TotalChildren)
          |
          v
Group Education and Marital_Status categories
          |
          v
Drop redundant / replaced columns
          |
          v
Inspect and filter selected outliers
          |
          v
Correlation analysis
          |
          v
One-hot encode Education and LivingWith
          |
          v
Standardize features with StandardScaler
          |
          +-----------------------------+
          |                             |
          v                             v
PCA to 3 components              Evaluate candidate K values
          |                      Elbow / WCSS and Silhouette
          v                             |
3D feature-space plots                 v
                                  Choose a candidate K
                                        |
                         +--------------+--------------+
                         |                             |
                         v                             v
                   K-Means                  Agglomerative Clustering
                         |                             |
                         v                             v
                 Cluster labels                 Cluster labels
                         |
                         v
                 Cluster summaries
